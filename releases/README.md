#Overview

This page outlines a standard workflow for updating Rho's Open Source projects. The process defined here is implemented entirely in GitHub. 

#Versions
##Semantic Versioning
Our open source projects use [semantic versioning](http://semver.org/). In short: 

> Given a version number MAJOR.MINOR.PATCH, increment the:
> 
> - MAJOR version when you make incompatible API changes,
> - MINOR version when you add functionality in a backwards-compatible manner, and
> - PATCH version when you make backwards-compatible bug fixes.

##GitHub releases
Releases are a standard feature in GitHub. We implement them to track version as follows: 
- _Releases_ (Required) - Each version of a library gets a release. The release ties the version to a snapshot of the source code (a commit). A    step-by-step guide to creating releases is [here](https://help.github.com/articles/creating-releases/). 
- _Milestones_ (Optional) - Milestones can be used to tie a set of issues to an upcoming version of the repository. A step-by-step guide to creating milestones is [here](https://help.github.com/articles/creating-and-editing-milestones-for-issues-and-pull-requests/).

More detail about how releases, milestones and tags are used at Rho is given in the [workflow](#release-workflow) section. 

#Issues
Development tasks (new features, technical tasks, bugs, etc.) should be tracked using issue tracking software. We typically use JIRA (for large, multi-developer projects) or GitHub issues (for smaller issues). 

The details about issue management vary from project to project, but, at a minimum, we track the following:
- Name
- Description
- Priority - Tracked with custom labels in GitHub. 
- Release version - Tracked with "Fix Version" in JIRA; "Milestone" in GitHub.
- Issue type - Tracked with custom labels in GitHub. 
- Assignee

#Release Workflow
Broadly speaking, work on a new version of a project occurs in 4 phases.

1. **Planning** - Outline features and make issues. 
2. **Development** - Code the new features in a branch. 
3. **Testing** - Test the new features. 
4. **Deployment** - Release the new features.

Workflow details vary from project-to-project, but guidance for each phase is provided below.

##Phase 1 - Planning
The team agrees on an approach for the planned changes and makes sure issues are created before coding begins.

- Make a general plan for what features are going in to the next release. No need to get this perfect. You can update as you're working, but it's good to have the team agree on an approach. (**Required**)
- Create issues describing the new features, and associate them with the milestone. If no issue exists, create one before committing code. (**Required**)
- Draft a new release for the version, with an overview of the updates. Versions should be called `vX.X.X`. Make sure to mark the release as a draft until the work is done.  Make sure you're following the semantic versioning guidelines when picking the version number. (*Recommended*)
- Create a milestone for the version, and assign the milestone to the relevant issues. The milestone should also be called `vX.X.X`. (*Recommended*)

##Phase 2 - Development
Once the team agrees on an approach and creates issues, the developer creates a new branch and updates the source code to implement new functionality.

- The developer creates a new branch for development work and notes the branch name on a comment in the issue(s). Please do not commit changes directly to the `master` branch, all new code should be committed to a new "feature branch". (**Required**).
- If using GitHub issues, mention the related issue number in each commit (*Recommended*). 
- Whenever possible, create a unit test for a new feature (*Recommended*)
- Run any existing unit tests on the feature branch before testing. (*Recommended*)
- Make sure that the feature branch is up to date with the `master` branch before testing. (*Recommended*)
- If applicable, make an example demonstrating new functionality. (*Recommended*)

##Phase 3 - Testing
New functionality is verified by an independent tester before release. 

- Once a new feature is implemented, it should be independently tested before being merged in to `master`. Testing should be conducted by someone other than the developer. (**Required**)
- Testing requirements vary for each project, but it is important to define a workflow. A sample GitHub-only workflow, that can be modified as needed, is given below. (*Required*)

Once all features for a new version are tested, we move to Phase 4, Deployment. 

### Sample Testing Workflow
 1. The developer creates a pull request once a feature branch is ready for testing.
 2. Developer comments on the pull requests with an @ mention, letting the tester know the branch is ready and provides instructions about how to access the updates (e.g. links to a GitHub gist) 
 3. The tester confirms the functionality or informs the developer about problems, via comments on the pull request. 
 4. Issues are closed once testing is complete. This can be done automatically using [this process](https://github.com/blog/1506-closing-issues-via-pull-requests)

##Phase 4 - Deployment
Once all issues in a given milestone have passed testing, the new features are ready to be released and deployed.

- To release a new version of a repository, the new features are merged in to the `master` branch and the new version of the library is released. (**Required**)
- The deployment process will vary for each project, but it is important to define a workflow. A sample GitHub-only workflow, that can be modified as needed, is given below. (*Required*)
- Regression testing is generally performed immediately before a release to make sure new features have not created any unexpected behavior. (*Recommended*)

### Sample Deployment Workflow
  1. Merge the pull requests for feature branches in to the master branch.
  2. Make any needed updates to the wiki.
  3. Make any updates to examples (or creates a new example to demonstrate new functionality and add it to the wiki).
  4. If there is a build process (like the once described [here](https://github.com/RhoInc/webcharts-wrapper-boilerplate/wiki)), make sure it is fully executed.
  5. If the package is being tracked via NPM, publish the new version following these steps:  
   1. Confirm that you have the latest version of the repo checked out on your computer
   2. Using a shell, browse to the root directory for the repo
   3. Login to npm via npm adduser --always-auth (at Rho use the rhographics username and password)
   4. Confirm that the package.json file is up to date (especially the version field)
   5. Publish the package by typing npm publish
  6. Reviews the draft release notes, and update as needed, and publish the release.
  7. Save a snapshot of the new version to https://graphics.rhoworld.com/src/ following the steps below (__coming soon__)

#Exceptions and Modifications
The processes described here represent a baseline guidance for open source projects at Rho, but project teams are encouraged to customize these methods as is appropriate for a given project. These customizations include: 

- Using JIRA instead of GitHub issues is fairly common in larger projects that implement SCRUM/Agile methodologies. 
- Several projects (like this one!) are primarily for documentation. These projects still use GitHub, but generally do not have versioned releases. 
- We use [GitHub flow](https://guides.github.com/introduction/flow/) which emphasizes making a new branch for each feature for larger multi-developer projects. For small single-developer projects, a single branch might be made for a release. 
