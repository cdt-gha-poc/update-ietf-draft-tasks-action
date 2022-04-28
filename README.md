# Update IETF Internet-Draft Tasks Github Action

This Github Action updates an existing IETF Internet-Draft Github repository's
Github Action workflows to match that of the [Create IETF Internet-Draft Github
Action](https://github.com/IRTF-HRPC/create-ietf-draft-repo-action).

More specifically, it updates the files in a repository's `.github/workflows`
folder that configure the validate, generate, and publish tasks.

* _validate_: Github Actions workflow that validates the Markdown draft, making
sure the generate step is possible
* _generate_: Github Actions workflow that creates the HTML, XML, and TXT
versions of a file written in Markdown
* _export_: Github Actions workflow that uploads the XML version of the draft to the IETF
Datatracker, which triggers a confirmation email

## Action Inputs

*release_version*: Version of the workflows in Create IETF Internet-Draft
Github Action to use. This can be a git reference, branch name, SHA, or other
tag. Defaults to 'main'.

## Setting Up This Action

### Requirements

You must have write access to the repository to add this action.

The draft file must be a Markdown file that matches the format `draft-*.md`.

### Quickstart

This action must reside in a Github repository in order to be used by a Github
Action. If you have an existing IETF Internet-Draft repository, please ensure
it meets the requirements above.

More details about Github Actions can be found in their
[documentation](https://docs.github.com/en/actions/learn-github-actions/introduction-to-github-actions).

Adding the following YAML file contents to the path indicated
(`{REPO_ROOT}/.github/workflows/update.yml`) will add this action to a
repository and enable manual runs.

```
# {REPO_ROOT}/.github/workflows/update.yml

TODO
```

Please see below for information on action versions.

## How To Run

After following the Quickstart instructions above for your draft repository, go
to the Actions tab and select Update draft tasks in the sidebar.

TODO screenshot

Under the workflow runs section there will be a button labeled Run workflow.
Clicking this brings up the option to override the `release_version`. If you
wish to set this to an older version, refer to the [Create IETF Internet-Draft
Github Action](https://github.com/IRTF-HRPC/create-ietf-draft-repo-action)
repository to find the relevant version name, then paste it here. Otherwise,
the most up to date version is used.

A successful run will be shown in green under the Actions tab. A failed run
will be shown in red, and link to it will be emailed to you.

TODO screenshots

## Action Versions

When this action is set up for a repo, it can either be pinned to a specific
version (ie. IRTF-HRPC/update-ietf-draft-tasks-action@v0.1) or left without
(ie. IRTF-HRPC/update-ietf-draft-tasks-action), which will default to the most
recently updated version. This action follows the principles of
[semantic versioning](https://semver.org/) and we version our releases
accordingly. We recommend you leave it as is to use the most up to date version.
