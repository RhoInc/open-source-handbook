#Overview

This page outlines a standard workflow for updating Rho's Open Source projects. The process defined here is implemented entirely in github. 

#Versions
##Semantic Versioning
Our open source projects use [semantic versioning](http://semver.org/). In short: 

> Given a version number MAJOR.MINOR.PATCH, increment the:
> 
> - MAJOR version when you make incompatible API changes,
> - MINOR version when you add functionality in a backwards-compatible manner, and
> - PATCH version when you make backwards-compatible bug fixes.

##Github releases
Releases are a standard feature in github. We implement them to track version as follows: 
- _Releases_ (Required) - Each version of a library gets a release. The release ties the version to a snapshot of the source code (a commit). A    step-by-step guide to creating releases is [here](https://help.github.com/articles/creating-releases/). 
- _Milestones_ (Optional) - Milestones can be used to tie a set of issues to an upcoming version of the repository. A step-by-step guide to creating milestones is [here](https://help.github.com/articles/creating-and-editing-milestones-for-issues-and-pull-requests/).

More detail about how releases, milestones and tags are used at Rho is given in the [workflow](#workflow) section. 

#Issues
Development tasks (new features, technical tasks, bugs, etc.) should be tracked using issue tracking software. We typically use JIRA (for large, multi-developer projects) or github issues (for smaller issues). 

The details about issue management vary from project to project, but, at a minimum, we track the following:
- Name
- Description
- Priority - Tracked with custom labels in Github. 
- Release version - Tracked with "Fix Version" in JIRA; "Milestone" in Github.
- Issue type - Tracked with custom labels in Github. 
- Assignee

#Release Workflow
Broadly speaking, work on a new version of a project occurs in 3 phases.

1. Planning
2. Development 
3. Testing
4. Deployment

Workflow details vary from project-to-project, but guidance for each phase is provided below.

##Phase 1 - Planning
The team agrees on an approach for the planned changes and make sure issues are created before coding begins.. 

- Make a general plan for what features are going in to the next release. No need to get this perfect. You can update as you're working, but it's good to have the team agree on an approach. (**Required**)
- Create issues describing the new features, and associate them with the milestone.If no issue exists, create one before commiting code. (**Required**)
- Draft a new release for the version, with an overview of the updates. Versions should be called `vX.X.X`. Make sure to mark the release as a draft until the work is done.  Make sure you're following the semantic versioning guidelines when picking the version number. (*Recommended*)
- Create a milestone for the version, and assign the milestone to the relevant issues . The milestone should also be called `vX.X.X`. (*Recommended*)

##Phase 2 - Development
Once the team agrees on an approach and creates issues, the developer creates a new branch and updates the source code to implement new functionality.

- The developer creates a new branch for development work and notes the branch name on a comment in the issue(s). Please do not commit changes directly to the `master` branch, all new code should be committed to a new "feature branch". (**Required**).
- If using github issues, mention the related issue number in each commit (*Recommended*). 
- If applicable, make an example demonstrating new functionality. (*Recommended*)

##Phase 3 - Testing
New functionality is verified by an independent tester before release. 

- Once a new feature is implemented, it should be independently tested before being merged in to `master`. Testing should be conductued by by someone other than the developer. (**Required**)
- A standard github-only testing workflow might follow the following process: (*Recommended*):  
 1. The developer creates a pull request once a feature branch is ready for testing.
 2. Developer comments on the pull requests with an @ mention, letting the tester know the branch is ready and provides instructions about how to access the updates (e.g. links to a github gist) 
 3. The tester confirms the functionality or informs the developer about problems, via comments on the pull request. 
 4. Issues are closed once testing is complete. This can be done automatically using [this process](https://github.com/blog/1506-closing-issues-via-pull-requests)

Once all features for a new version are tested, we move to Phase 4. 


##Phase 3 - Deployment
Once all issues in a given milestone have passed testing, the new features are ready to be deployed. The developer does the following: 

- Merge the pull requests in to the master branch.
- Make any needed updates to the wiki.
- Make any updates to examples (or creates a new example to demonstrate new functionality and add it to the wiki).
- If there is a build process (like the once described [here](https://github.com/RhoInc/webcharts-wrapper-boilerplate/wiki)), make sure it is fully executed.
- If the package is being tracked via NPM, publish the new version following these steps:  
 1. Confirm that you have the latest version of the repo checked out on your computer
 2. Using a shell, browse to the root directory for the repo
 3. Login to npm via npm adduser --always-auth (at Rho use the rhographics username and password)
 4. Confirm that the package.json file is up to date (especially the version field)
 5. Publish the package by typing npm publish
- Reviews the draft release notes, and update as needed, and publish the release.
- Save a snapshot of the new version to https://graphics.rhoworld.com/src/ following the steps below (__coming soon__)

#Exeptions and Modifications
The processes described here represent a baseline guidance for open source projects at Rho, but project teams are encouraged to customize these methods as is appropriate for a given project. These customizations include: 

- Using JIRA instead of github issues is fairly common in larger projects that implement SCRUM/Agile methodologies. 
- Several projects (like this one!) are primarily for documentation. These projects still use github, but generally do not have versioned releases. 
- We use [github flow](https://guides.github.com/introduction/flow/) which emphasizes making a new branch for each feature for larger multi-developer projects. For small single-developer projects, a single branch might be made for a release. 
