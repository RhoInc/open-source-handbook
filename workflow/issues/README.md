#Issue workflow
This page outlines a workflow for working on issues in github. Note that this process is almost always completed within the context of the [release workflow](https://github.com/RhoInc/open-source-handbook/workflow/releases/README.md) The process defined here is implemented entirely in GitHub, and is in use with several of Rho's repositories focusing on interactive data visualization.


#Github Issues
Development tasks (new features, technical tasks, bugs, etc.) should be tracked using github issues. The details about issue management vary from project to project, but, at a minimum, we track the following:
- Name
- Description
- Release version - "Milestone" in GitHub
- Assignee

#General Guidance
We generally use the following guidelines for issue work: 
- The project team should thoroughly outline the task details in the issue and the issue should be QCed by another member of the team.
- Developers should prioritize issues in upcoming releases. 
- Each issue should have its own branch/pull requests. Very similar issues can be grouped in a branch/PR as needed as long as it's well documented. The pull request should always reference the issue(s) and vice-versa. This is [easy in github]() <- link to guide
- Requirement discussion should happen on the issue, technical discussion should happen on pull requests, but some overlap is fine. 
- Requirements should be clearly documented in the issue _before_ starting to code. 

#Workflow
Again, issue work is generally nested in the [release workflow](). Once an issue has a release and a developer assigned, we generally follow the workflow below: 

1. Discuss any requirement/implementation questions on the issue. 
2. Once approach is clear, Dev creates new branches/PRs as needed for the issue. Issue branches should be merged in to the dev branch (e.g. `v1.3.0`), _not_ directly in to master. Dev should be sure to link the issue and the PR. 
3. Dev discusses technical questions on PR. 
4. Once Dev code is finalized, they tag a different dev for code review. They discuss/update code as needed.
5. Once code review passes, the developer @comments tester in PR with notes on testing.
6. Hopefully test steps are clear from comments on issue/PR, but tester asks questions in comments as needed. In complicated cases, testers should document test steps in a comment on the PR.
7. Test steps should be approved by a dev before the tester runs the test on the issue.
8. Once testing passes, tester @comments dev. Dev merges pull request in to dev branch for the release. 
