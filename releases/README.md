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

##Github releases and milestones
Releases, milestones and tags are all standard features in github. We implement them to track version follows: 
- _Releases_ - Each version of a library gets a release, which ties the version to a snapshot of the source code (a commit). A    step-by-step guide to creating releases is [here](https://help.github.com/articles/creating-releases/). 
- _Milestones_ - Each version of a library also gets a milestone. A milestone is used to tie a set of issues to an upcoming version of the software. A step-by-step guide to creating milestones is [here](https://help.github.com/articles/creating-releases/).

So, each version of our repositories gets both a milestone and a release. More detail about how releases, milestones and tags are used at Rho is given in the [workflow](#workflow) section. 

#Issues
All development tasks (new features, technical tasks, bugs, etc.) are tracked as github issues. Milestones are used to group issues according to version. Labels are used for to organize priority and issue type as follows: 

- Priority - Labels for "Low Priority" and "High Priority" are used as needed. 
- Issue Type - "Bug", "Enhancement","Documentation" and "New Feature" labels are used to indicate the type of issue. 
 
Generally speaking, milestones are required, but labels are optional. 

#Release Workflow
Broadly speaking, work on a new version of a project occurs in 3 phases.

1. Planning
2. Development & Testing
3. Deployment

Details about the phases is provided below.

##Phase 1 - Planning
First, determine what will be included in the new release and make sure issues provide enough detail for a developer. Complete the following steps in this phase: 

- Determine what the new version number will be based on the semantic versioning guidelines above. 
- Draft a new release for the version, with an overview of the updates. Versions should be called `vX.X.X`. Make sure to mark the release as a draft until the work is done. 
- Create a milestone for the version. The milestone should also be called `vX.X.X`.
- Create issues describing the new features, and associate them with the milestone.
- Assign the issues to the developer(s) who will complete the tasks. 
- Developers should review the issues and follow-up with any questions. Comments on the issues, with appropriate @ mentions, are a good place for the discussion. 
 
Once the issues are well defined, the release can more to Phase 2. 

##Phase 2 - Development & Testing
Here the developer updates the source code to implement new functionality described in the issues using the following process: 

- The developer creates a new branch for development work and notes the branch name on a comment in the issue(s).
- The developer commits changes to resolve the issue in the branch and mentions the related issue number in each commit.
- The developer "deploys" the branch so that a tester can confirm functionality. This is most commonly done using a github gist. Note the location in the issue(s). 
- The developer creates a pull request with a note that will automatically close the issue(s) once the pull request is merged ([see details](https://github.com/blog/1506-closing-issues-via-pull-requests)). 
- The developer informs the tester that the pull request is ready via an @ comment on the pull request. 
- The tester confirms the functionality or informs the developer about problems, via comments on the pull request. 

Once all issues in the milestone for a given release have passed testing, we move to Phase 3. 

We use [github flow](https://guides.github.com/introduction/flow/) which emphasizes making a new branch for each feature for larger multi-developer projects. For small single-developer projects, a single branch might be made for a release. 

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
