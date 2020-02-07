# Release Workflow

This page outlines a workflow for releasing new repository versions in GitHub. The process defined here is implemented entirely in GitHub, and is in use with several of Rho's repository focusing on interactive data visualization. 

## Semantic Versioning
These Projects use [semantic versioning](http://semver.org/). In short: 

> Given a version number MAJOR.MINOR.PATCH, increment the:
> 
> - MAJOR version when you make incompatible API changes,
> - MINOR version when you add functionality in a backwards-compatible manner, and
> - PATCH version when you make backwards-compatible bug fixes.

## GitHub releases
Releases are a standard feature in GitHub. We implement them to track version as follows: 
- _Releases_ - Each version of a library gets a release. The release ties the version to a snapshot of the source code (a commit). A step-by-step guide to creating releases is [here](https://help.github.com/articles/creating-releases/). 
- _Milestones_  - Milestones can be used to tie a set of issues to an upcoming version of the repository. A step-by-step guide to creating milestones is [here](https://help.github.com/articles/creating-and-editing-milestones-for-issues-and-pull-requests/).

More details about how releases, milestones and tags are used are given in the Workflow section below. 

## Issues
GitHub issues and pull requests are used to track the work done in a release. See the [Issues workflow](https://github.com/RhoInc/open-source-handbook/blob/master/workflow/issues/README.md) for more detail.

## Release Workflow
The process for planning, developing, testing and deploying a new version of an existing repo is outlined below. 

1. Create a milestone with the version number for the release (you can always tweak the version number later if the scope changes). 
2. Populate the milestone with new and existing issues. 
   - Create new issues as needed. 
   - Tag each issue with the milestone.
   - It's good practice to review all existing issues for the project (i.e. the backlog) at this time as well.
   - Assign all issues to be included in the release to a developer
3. Create a "development branch" for the new version (`git checkout -b "v1.3.0-dev"`)
4. Change the version number in package.json and commit and push the change to the new branch (`git commit -a -m "updated version to v1.3.0"` and `git push --set-upstream origin v1.3.0`)
5. Create a pull request for the new development branch
   - Target branch should be `master`
   - Confirm that the master branch is protected, and that a review is required before merging to master. 
6. Add the pull request to the overall [GitHub project](https://github.com/orgs/RhoInc/projects/1) for tracking releases.
7. Begin to work on the release. Updates to the codebase should be developed and tested in Feature Branches, which are merged into the dev branch when complete. For more details about working on issues, see the [issue workflow](https://github.com/RhoInc/open-source-handbook/blob/master/workflow/issues/README.md)
7. Once all issues are resolved, the dev branch should be reviewed. The exact review process may vary from project to project, but options include: Code review, automated tests, regression testing, etc.
8. Once testing is complete, the dev branch/pull request can be merged in to master. 
9. The wiki should be updated to document new functionality. 
10. Publish release with descriptive releases notes in GitHub
11. If the package is being tracked via NPM, publish the new version following these steps:  
     1. Confirm that you have the latest version of the repo checked out on your computer.
     2. Using a shell, browse to the root directory for the repo.
     3. Login to npm via npm adduser --always-auth (at Rho use the rhographics username and password).
     4. Confirm that the package.json file is up to date (especially the version field).
     5. Publish the package by typing npm publish.
