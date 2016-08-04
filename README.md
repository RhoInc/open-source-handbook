# Rho Open Source Guide

## Overview

This library provides information about open source software development at [Rho](http://www.rhoworld.com). We provide a brief overview of Rho's philosopy regarding open source development, and then give guidelines for Rho staff and external contributors working on Rho's open source projects. 

Planned updates to this document are tracked as [github issues](https://github.com/RhoInc/open-source-guide/issues). Questions can be submitted on the issues page or via [email](mailto:opensource@rhoworld.com).

## What is open source?

The [Open Source Initiative](https://opensource.org/) has a good [definition](https://opensource.org/faq#osd):

> Generally, Open Source software is software that can be freely accessed, used, changed, and shared (in modified or unmodified form) by anyone.

## What is Rho's position on open source code sharing?

[Rho](http://www.rhoworld.com/) is in favor of open source code sharing. An open source approach takes the work done at Rho and broadens its reach. That's a great thing since it falls in line with our our core purpose: 

> To improve health, extend life, and enhance quality of life through corporate and research excellence.

## What is currently being done at Rho?

More than a dozen open source projects are publicly available on [our GitHub page](https://github.com/RhoInc), and many more are under development. Contact [opensource@rhoworld.com](mailto:opensource@rhoworld.com) if you have questions or want to get involved.

The rest of this document provides more details about the strategic benefits of open source projects and provides guidelines for how they should be created and maintained at Rho.

# Rho's Open Source Strategy

## Guiding principle

When possible, code should be made public.

## Motivations/Business Value

*Core Values* – Open source development reflects [Rho's Core values](http://www.rhoworld.com/rho/about/our-values). _A team culture_, _critical and creative thinking_, and _innovation_ are at the heart of the open source philosophy. We demonstrate our _integrity_ and _quality_ by releasing the details of our process and allowing others to examine and enhance our work. The open source process encourages _agility and adaptability_, _profitability_, and _stability_ by encouraging thorough documentation, reducing rework, and increasing the visibility of our work.

*Process Improvements* – Many of the benefits of the open source process hold true even if a project is never publicly released and the audience is only our fellow employees. Developing a tool as if it could become open source, even if we doubt it ever will, has value because it can foster engagement across sectors and it prompts you to develop tools with other users in mind. This approach also helps you avoid rework should your project be converted to open source later.

*Community* – Open source projects create valuable relationships with the broader research community that can expand our perspective, improve our work, and potentially lead to new work for Rho.

*Scientific* – More openness [promotes better science](https://opensource.com/education/11/10/default-open-scientific-method).

*Publication* – Reproducibility is an increasingly important topic in scientific journals, with recent meta-analyses showing that a large percentage of results can&#39;t be reproduced. As a result, many top journals are now recommending or requiring data and/or code to be submitted along with manuscripts.

*Policy* – [The Open Government initiative] (https://www.whitehouse.gov/open/) which began in 2009 is pushing for more openness and transparency in government, and recently led to a draft [federal source code policy] (https://sourcecode.cio.gov/) that would mandate code sharing for federally funded research.

*Professional Development* – Working on an open source project can be a form of on-the-job professional development. It is a great way to keep up with external innovations and open source projects serve as great "work samples" on a resume.

# Developer Guidance

## Should my project be open source?

A variety of projects at Rho are suitable for open source development. The checklist below lists attributes that indicate if your project may be a good candidate for open source, however this is not meant to be prescriptive or exhaustive.

- Benefits others outside of Rho
- Developed with federal or overhead funds
- Developed using existing open source technology (e.g., JavaScript, D3, R)
- Improves the way other people use a tool (e.g., SAS macro)
- Can be packaged without giving away private or proprietary information about Rho
- You are planning to present or publish the code (or work directly referencing the code) at a conference or in a journal
- You would like feedback on your code, including ways it can be improved

If you think your project would be a good candidate for open source release, contact us at [opensource@rhoworld.com](mailto:opensource@rhoworld.com).

## Step-by-step guide for open source projects at Rho

Creating and maintaining an open source project is a collaboration between the _Project Owner_ and _Rho's Open Source Committee_. This section describes 4 phases of open source development and outlines who is responsible for each part of the process.

### Phase 1 – Project Set-up 

_Responsible parties_: Project Owner & Open Source Committee

1. To set up a new open source project, the Project Owner [emails the Open Source committee](mailto:opensource@rhoworld.com) with the following information: 
 - A brief description of the project
 - Sponsor of the project
 - Who is working on the project? 
 - Current status of the project (e.g. "Proposal sent to NIAID on 10/9/2016" or "Internal library is active use. See s:/my/project/path/")
 - Brief rationale for making the project open source

2. Open Source Committee reviews the proposal and either approves or contacts owner to discuss

3. Once approved, the private project is set up on GitHub.
  - If needed, the Project Owner obtains a GitHub account and requests access to the [RhoInc GitHub organization](https://github.com/RhoInc)
  - The Open Source Committee creates a new private repository including a set of standard files from a basic template and gives access to any needed developers.

### Phase 2 – Code and Documentation preparation 

_Responsible parties_: Project Owner

The Project Owner and their collaborators create/move all needed code and documentation to GitHub. See the Content Guidelines section below for more details.

### Phase 3 – Review process

_Responsible party_: Open Source Committee

Once the content is ready for initial release, the Project Owner notifies the Open Source Committee. The Open Source Committee assigns a reviewer, and the committee comments/approves. If possible, the GitHub project is made public at this time.

### Phase 4 – Maintenance

_Responsible party_: Project Owner and Open Source Committee

The Project Owner is responsible for maintaining the project, which includes responding to any issues or pull requests from other users - with special priority given to requests from outside Rho; the Open Source Committee can support these efforts as needed. The Open Source Committee will conduct periodic reviews of updates to existing projects, and will contact the Project Owner with questions as needed.

# Content Guidelines and Resources

## Getting Started with Open Source Development 

Users should be familiar with open source development in general, GitHub in particular, before starting their first project. Here are some good links to get familiar with the basics:

- [Open Source](https://opensource.com/resources/what-open-source)
- [GitHub Guides](https://guides.github.com/) (especially [Hello World with GitHub](https://guides.github.com/activities/hello-world/))

Users should also review some of our existing open source projects:

- [Webcharts] (https://github.com/RhoInc/Webcharts) - A javascript library with a multi-page wiki and more than 20 releases.
- [SAS Axis Macro](https://github.com/RhoInc/sas-axismacro) - A SAS macro for automating the selection of axis ranges for continuous variables.
- [CASI Minimally Important Difference Simulation](https://github.com/RhoInc/CASI_MID) - Supplemental materials and code giving details about a statistical simulation conducted in support of a manuscript submission.

## Basic Required Content

Several types of content are required for Rho's open source projects. In particular:

- *Code* – The source code for your program should be posted to GitHub and should follow programming best practices.
- *Documentation* – Stand-alone documentation should be included in the form of a README.md and/or a wiki. Documentation should include instructions on how to use the library, requirements, and configurable settings.
- *Examples* – Stand-alone examples that the user can reproduce independently should be included, demonstrating the primary use cases for the library; these can be included as part of the wiki or as [GitHub gists](https://help.github.com/articles/about-gists/). Examples should follow the data guidelines given below.
- *License* – A license.md should be inluded in for all projects. Rho's preferred license for open source software is the [MIT license](https://opensource.org/licenses/MIT).

## Data guidelines

No private or confidential data should be included in an open source project or it's associated examples. Guidelines include:

- No private or confidential data
- No personal identifiers
- De-identified data from Federal studies may be used if the data has already been released publicly and there are no embargoes on data sharing
- When in doubt, consider using publicly available data for examples. Several repositories exist including
  - [data.gov](https://www.data.gov/)
  - Reddit ( [1](https://www.reddit.com/r/datasets/top/), [2](https://www.reddit.com/r/opendata/top/))

**Use an abundance of caution when sharing data.** Contact [opensource@rhoworld.com](mailto:opensource@rhoworld.com) if you have any doubt. 

## GitHub and other Tools

Our open source projects are hosted at [https://github.com/RhoInc](https://github.com/RhoInc). GitHub has built-in procedures for many common activities in open source development including version control, issue tracking, and release management.

The exact process used to create and maintain a project can vary as long as the basic content described above is present and the style guides are followed. However, some recommended best practices have emerged and are listed below for reference:

- Release process: [GitHub Releases](https://github.com/blog/1547-release-your-software)
- Issue Tracking: [GitHub Issues](https://guides.github.com/features/issues/)
- Versioning: [Semantic Versioning](http://semver.org/)
- Testing overview: _Coming soon_
- Code Review Tools: _Coming soon_
- Coding Guidelines: _Coming soon_
- Code Style Guides: _Coming soon_
- Development Workflow: [GitHub flow](https://guides.github.com/introduction/flow/) _(Advanced)_
- Deploy Process/Continuous Deployment: [TeamCity](https://www.jetbrains.com/teamcity/) _(Advanced)_

# FAQ

## What are my obligations after sharing my project?

One of the benefits of sharing a project open source is it allows others to refine, adapt, and improve upon your code.  When you release open source, you should be willing to engage other users if they have questions, identify errors, or propose changes to your code. For the majority of projects, this is a very minimal time commitment (and many projects never receive any feedback), but you should be prepared to interact with other users if they are interested in your tool. It is also a good idea to review your project over time to see if you could enhance it or improve upon it. As new technologies become available, you may want to update your code to keep it relevant or to add new features.

## I'm not a programmer. Can I contribute to open source projects?

Sure! Check out [this link](https://opensource.com/business/14/12/8-ways-contribute-open-source-without-writing-code) for ideas and then contact us to discuss.

## What is Rho's preferred license for open source projects?

The MIT license.

## Answers coming soon
- What are the costs and drawbacks of open source development?
- Is this like data sharing? 
- What types of code are appropriate for open source?
