#Overview

This page outlines a standard workflow for updating Rho's Open Source projects. The process defined here is implemented entirely in github. 

#Versions
##Semantic Versioning
Our open source projects use [semantic versioning](http://semver.org/). In short: 

> Given a version number MAJOR.MINOR.PATCH, increment the:
> 
> MAJOR version when you make incompatible API changes,
> MINOR version when you add functionality in a backwards-compatible manner, and
> PATCH version when you make backwards-compatible bug fixes.

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

##Phase 1 - Planning

##Phase 2 - Development

##Phase 3 - Testing

##Phase 4 - Deployment

#Exeptions and Modifications
The processes described here represent a baseline guidance for open source projects at Rho, but project teams are encouraged to customize these methods as is appropriate for a given project. These customizations include: 

- Using JIRA instead of github issues is fairly common in larger projects that implement SCRUM/Agile methodologies. 
- Several projects (like this one!) are primarily for documentation. These projects still use github, but generally do not have versioned releases. 


