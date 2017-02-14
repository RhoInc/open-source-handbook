# Rho Open Source Handbook

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

*Policy* – [The Open Government Initiative] (https://www.whitehouse.gov/open/) which began in 2009 is pushing for more openness and transparency in government, and recently led to a draft [federal source code policy] (https://sourcecode.cio.gov/) that would mandate code sharing for federally funded research.

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

# Workflows

Details regarding suggested workflows for open source development at Rho are documented here:
- [Open Source Committee](workflow/opensourcecommittee/README.md)
- [Release](workflow/releases/README.md)
- [Issues](workflow/issues/README.md)  

# Content Guidelines and Resources

## Getting Started with Open Source Development 

Users should be familiar with open source development in general, GitHub in particular, before starting their first project. Here are some good links to get familiar with the basics:

- [Open Source](https://opensource.com/resources/what-open-source)
- [GitHub Guides](https://guides.github.com/) (especially [Hello World with GitHub](https://guides.github.com/activities/hello-world/))

Users should also review some of our existing open source projects:

- [Webcharts](https://github.com/RhoInc/Webcharts) - A javascript library with a multi-page wiki and more than 20 releases.
- [SAS Axis Macro](https://github.com/RhoInc/sas-axismacro) - A SAS macro for automating the selection of axis ranges for continuous variables.

## Basic Required Content

Several types of content are required for Rho's open source projects. In particular:

- *Code* – The source code for your program should be posted to GitHub and should follow programming best practices.
- *Documentation* – Stand-alone documentation should be included in the form of a README.md and/or a wiki. Documentation should include instructions on how to use the library, requirements, and configurable settings.
- *Examples* – Stand-alone examples that the user can reproduce independently should be included, demonstrating the primary use cases for the library; these can be included as part of the wiki or as [GitHub gists](https://help.github.com/articles/about-gists/). Examples should follow the data guidelines given below.
- *License* – A license.md should be inluded in for all projects. Rho's preferred license for open source software is the [MIT license](https://opensource.org/licenses/MIT).

## Data guidelines

**Use an abundance of caution when sharing data. Review all Rho SOPs and policies, which take precedence over this document. Contact [opensource@rhoworld.com](mailto:opensource@rhoworld.com) if you have any questions.**

No private or confidential data should be included in an open source project or it's associated examples. Guidelines include:

- No private or confidential data
- No personal identifiers
- De-identified data from Federal studies may be used if the data has already been released publicly and there are no embargoes on data sharing
- When in doubt, consider using publicly available data for examples. Several repositories exist including
  - [data.gov](https://www.data.gov/)
  - Reddit ( [1](https://www.reddit.com/r/datasets/top/), [2](https://www.reddit.com/r/opendata/top/))



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

One of the benefits of sharing a project open source is it allows others to refine, adapt, and improve upon your code.  When you release open source, you should be willing to engage other users if they have questions, identify errors, or propose changes to your code. For the majority of projects, this is a very minimal time commitmen, but you should be prepared to interact with other users if they are interested in your tool. It is also a good idea to review your project over time to see if you could enhance it or improve upon it. As new technologies become available, you may want to update your code to keep it relevant or to add new features.

## I'm not a programmer. Can I contribute to open source projects?

Sure! Check out [this link](https://opensource.com/business/14/12/8-ways-contribute-open-source-without-writing-code) for ideas and then contact us to discuss.

## What is Rho's preferred license for open source projects?

The [MIT license](https://opensource.org/licenses/MIT).

Licenses should be copyrighted for the year the tool is released, and any subsequent years that see a release.  For example, v1.0 of a tool was released in 2015, but has not had any subsequent updates, use "Copyright (c) 2015 Rho Inc."  However, if that same tool had a subsequent release of v1.1, v1.2, and v2.0 in 2016, use "Copyright (c) 2015-2016 Rho Inc." 

## How should I give credit for contributions and borrowed content in my project?

Open source can be confusing when it comes to intellectual property, but luckily there are a few ways to credit content. First, GitHub keeps an audit trail for commits made to your repo by other users, keeping track of who has worked on the project. While that list does capture the work that has been done, it is also good practice to include a list of contributors on the bottom of the first page in your wiki. This list should capture external collaborators, links to borrowed content, and attributions for repo inspiration. When copying and pasting code in the repo itself, it is best practice to include a link to the content's original source in a comment.

## When editing a wiki, can I edit it online directly or should I make a local copy and push the edits to master when I'm done?

It is preferred that you clone a local copy if you are making significant changes to your wiki to avoid potential confusion with your audience. If you opt to make a minor change to your wiki, you can do it directly on the wiki, but please include the following note, "This wiki is in development" to the top of the wiki, just below the title, while you work.

## What should I name my repo?

According to GitHub's Git Style Guide and the precedence set here at Rho, the following are considered best practices for naming a repo:
- General
 * Use short, descriptive names
 * Use dashes to separate words
 * Use lowercase throughout
- R
 * Avoid hyphens
 * Match project name to package 
- SAS
 * Use sas-"name" to be consistent with existing sas repos
		
Additionally, ideal repo names are:
- Descriptive
- Readable
- Consistent
- Contextual
- Future-friendly
- Extensible
- Reusable

## What are the costs and drawbacks of open source development?

Some of the biggest concerns with open source have to do with the fact that the tools are freely available, which impacts both developers and users.
* Developers - you may not get any direct financial compensation for your work.  [Several successful business models](https://handsontable.com/blog/articles/5-successful-business-models-for-web-based-open-source-projects) exist for open source tools, but unless you're actively implementing such an approach, there's little way to make money off ot it. 
* Users - the fact that the tools are free means there may be limited incentive for the developer to maintain the tools or provide technical support if you find problems. The best way to find reliable tools is look for tools that are have a lot of forks, are in continual development (have frequent releases), or those that have a large community of contributors.

Check out [this brief article](http://entrepreneurhandbook.co.uk/open-source-software/), which lists a few other pros and cons of working with open source software.

## Is this like data sharing?

Sort of. The concepts of open source and open data are very similar.  They are both predicated on the ideas of transparency, free use, and community benefit.  Open source sharing tends to be focused on sharing code and related resources (e.g., documentation) whereas data sharing is, as the name suggests, more focused on sharing a data set.  One important disctinction for data sharing, especially for data that comes from humans, is that there are important rules that dictate which data can be shared.  For example, the [Health Insurance Portability and Acountability Act (HIPAA)](https://www.hhs.gov/hipaa/) places strict rules on protecting personal health information and preventing this information from being shared without expressed permission of individuals and/or special considerations to de-identify and anonymize data so records cannot be tied back to an individual.

## What types of code are appropriate for open source

Any code that you create can be shared - software, web-based tools, statistical and analytical programs, database management programs, APIs, etc. If you code it, you can share it.  
