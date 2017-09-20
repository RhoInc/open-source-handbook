# Oversight Workflows

This page documents the process for creating and maintaining open source repositories at Rho. Generally speaking, the Open Source Committee is here to support repository owners and provide high-level quality control for Rho's open source projects. 

## Workflow for Open Source Projects at Rho

Creating and maintaining an open source project is a collaboration between the _Project Owner_ and _Rho's Open Source Committee_. This section describes 4 phases of open source development and outlines who is responsible for each part of the process.

### Phase 1 – Project Set-up 

_Responsible parties_: Project Owner & Open Source Committee

1. To set up a new open source project, the Project Owner [emails the Open Source committee](mailto:opensource@rhoworld.com) with the following information: 
 - A brief description of the project
 - Who will be working on the open source implementation
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

**Checklist for New Repos**

1. There is a decent readme

2. There is a license (MIT standard - permission required to use another license)

3. There is a decent wiki:
 - Explains the tool and it's intended use
 - Provides any parameters or need-to-know information
 - Logical flow of information
 - If multiple pages, logical organization
  
4. There are 1+ decent examples
	- Preferably a gist
  
5. There is a release documented in GitHub

6. Owner has confirmed that there is no confidential information in the repo

7. Code review been completed.

### Phase 4 – Maintenance

_Responsible party_: Project Owner and Open Source Committee

The Project Owner is responsible for maintaining the project, which includes responding to any issues or pull requests from other users - with special priority given to requests from outside Rho; the Open Source Committee can support these efforts as needed. The Open Source Committee will conduct periodic reviews of updates to existing projects, and will contact the Project Owner with questions as needed.

**Checklist for Maintaining Repos**

1. Pull requests have been maintained

2. Links are still functional

3. License is current

4. Releases are current

5. Examples are relevant and functional

6. There is a release documented in GitHub

7. Owner has confirmed that there is no confidential information in the repo

8. Code review been completed.
