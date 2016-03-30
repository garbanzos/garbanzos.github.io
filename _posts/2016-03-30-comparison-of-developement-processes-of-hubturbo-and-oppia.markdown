---
layout: post
title:  "Comparison of development processes of HubTurbo and Oppia"
date:   2016-03-30 13:42:02 +0800
categories: jekyll update
---

In this post, I will be comparing the development processes of [HubTurbo][hubturbo-github] and [Oppia][oppia-github]. 

### Getting Started

**Hubturbo**<br>
New contributors for HubTurbo can start contributing immediately after setting up the project and requested to select an issue labelled `forFirstTimers` as their first issue. 

**Oppia**<br>
New contributors for Oppia are required to sign a Contributor License Agreement (CLA) and fill in a short survey to indicate the parts of the codebase they are interested in (frontend, backend, tests etc.). Shortly after submitting the forms, the maintainers of the Oppia project personally emailed the contributors. In the email, the maintainers pointed the contributors to Oppia's contributor's guide and requested them to introduce their backgrounds and interests in order to match them to issues. 

**Discussion and Recommendations**<br>
Between the two projects, the Oppia community appear to be more welcoming. The personal email from the project maintainers made me feel like I was really welcomed to the Oppia community. Furthermore, the project maintainers seems to be really helpful to new contributors. They attempted to match me to issues that I may be interested in, in case I did not know where to start. 

On the other hand, HubTurbo seems less welcoming in comparison - there is no official welcome to HubTurbo and contributors immediately start on a `forFirstTimers` issue. However, upon closer inspection, you will find that most of the contributors of HubTurbo are already from the same community - NUS, School of Computing. This means many of the contributors may already know each other so there is no need create additional bureaucracies by requesting new contributors introduce themselves etc. This is in contrast with Oppia where new contributors usually do not know any of the existing contributors. 

Thus, in my opinion, two projects expect different types of contributors and should continue their respective approaches for this matter. 

### Setting Up 

**Hubturbo**<br>
Its readme.md directed contributors to the developer guide that contained intructions for set up. The instructions were really straightforward and easy to follow.  

**Oppia**<br> 
Its readme.md contained a short summary of the instructions for set up and had a link to the full instructions.    

**Discussion and Recommendations** CAN IMPROVE <br> 
In my opinion, Oppia's short summary of set up instructions is great for a new contributor who is already familiar with the project's stack. He can set up the project quickly with the essential steps described in the  projects' readme.md and does not have to read the details in the full set up instructions that he might already know. Currently, HubTurbo's readme.md does not contain a brief summary of the set up instructions but I feel that they can consider including it. 

### Development Process 

**Hubturbo**<br>
The development cycle of HubTurbo usually start with the selection an issue in the issue tracker or creation of a new issue that the contributor wish to fix. The contributor would then fix the issue on a branch of his forked repository. Once the issue is fixed, the contributor creates a PR. These branch, PR and description of PR must follow a strict naming rule that is described in the developer guide. After the PR is submitted, the contributor will receive suggestions for his code from a reviewer and is supposed to improve his code until it is of a certain standard. Once the merge is approved, the PR is merged by the reviewer (or the contributor if he has push access).  

**Oppia**<br>
The development cycle of Oppia is similar to HubTurbo, except the contributors do not have a strict convention to follow for the branch name, PR title and PR description.  

**Discussion and Recommendations**<br>
As a result of the lack of standard format of PRs, Oppia's [PR page][oppia-pr] is not very organised. Some of the PRs fail to reference the issue they are attempting to fix. This caused some contributors to submit PRs to fix the same issue because they are not aware that there is a PR already submitted to fix the issue. 

On the other hand, HubTurbo requires a PR follows these rules: 

- The name of the PR should be in the format "TITLE #X" 
- The description of the PR should include the text "Fixes #X" <br>

where TITLE is the title of the issue you selected, and X is its number. 
As a result of this standard format, there was little duplication of effort as contributors can easily find out whether someone else is already solving an issue by doing a search with the issue's title on HubTurbo's [PR page][hubturbo-pr]. 

Hence, for this aspect, I feel that Oppia can try to adopt some of HubTurbo's practises to reduce duplication of effort. 

[hubturbo-github]: https://github.com/hubturbo/hubturbo 
[oppia-github]: https://github.com/oppia/oppia
[oppia-pr]: https://github.com/oppia/oppia/pulls
[hubturbo-pr]: https://github.com/hubturbo/hubturbo/pulls 



