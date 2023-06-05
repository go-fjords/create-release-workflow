# create-release-workflow

Workflow for creating a tag, and a release with a changelog.
Afterwards it posts a slack message with the changelog.

## Development

### Releasing

#### Create release

Each release has its own Git *tag*. Do these steps to create a new release:

1. Create the tag: `git tag <version>`
1. Push the tag to origin: `git push origin <version>`


#### Update release

Because the release is now tagged to a specific commit, if you want to update the release, the tag has to be destroyed and re-created:

1. Delete the tag: `git push origin --delete <version>`
1. Delete the local tag: `git tag -d <version>`
1. Create the tag again: `git tag <version>`
1. Push the tag to origin: `git push origin <version>`
