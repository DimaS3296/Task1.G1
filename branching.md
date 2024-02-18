Basic commands for Branching:

[git branch](./branch.md)

[git checkout](./checkout.md)

 [git merge](./merge.md)

  [git rebase](rebase.md)




Branching is an essential feature in Git and version control. It allows developers to work on new features or bug fixes independently without affecting the main codebase. 

GIT branching strategies are patterns or approaches that tech teams use to organize & manage their code through different branches in a GIT system.

Each strategy defines the rules and guidelines for the creation, naming and merging the branches for facilitating collaboration, stability andrelease management.

1. #### Master branch

This is the main branch and one of the repository in which we have the latest stable code of production.  

2. #### Integration branch

This is the most important and active branch of the repository from which we make releases to the production server.

3. #### Staging branch

This is another stable branch of the repository for QA (quality assurance)-environment from which we make releases to the QA server. 

4. #### Dev-deploy branch

This branch will be used primarily for deploying on-going development work to the Dev environment. Since multiple teams may work on different features, projects and bugs at the same time, all of them need a Dev environment to test the changes before moving to QA. The idea of the Dev-deploy branch is to merge multiple feature branches to a common branch and deploy the same.
This is so that everyone can use a shared development environment at the same time to validate changes.

***Centralized Workflow***  
There's typically a single main branch in this strategy where developers commit   ([git commit](./commit.md))  directly.
Generally used for small projects for a small set of contributors.
Collaboration happens by committing changes directly to the main branch.

***Feature Branch Workflow***

The developers create a separate branch for each feature that they're working on.
Each feature branch is independent & can be developed and tested without disturbing the main branch.
Collaboration occurs by merging  feature branches into the main branch.

***GitFlow***

It is a branching strategy in GIT that defines specific branches for various stages of development.
It includes main branches for production-ready code, and other branches for on-going development.
    Feature, release and hotfix branches are used to facilitate collaboration.


***GitHub Flow***

GitHub Flow is a simple and lightweight Git branching strategy. It is well-suited for small teams and projects and a good choice for teams that need to release new features and bug fixes quickly.

The strategy is often used in conjunction with GitHub, a popular Git hosting service. The main idea of GitHub Flow is to keep the main branch always deployable. The emphasis is on small, frequent commits and feature branches for new development.


***GitHub Flow Workflow***

The GitHub Flow workflow uses only two branches:

**main.** 

The GitHub Flow workflow begins with the main branch that contains the latest stable code ready for release.

**feature.**
    
Developers create feature branches from the main branch to work on new features or fix bugs. Once a feature is complete, the feature branch is merged back into the main branch. In case of a merge conflict, developers must resolve it before completing the merge.

Once the merge is complete, the developer deletes the feature branch, keeping the repository clean and organized.

     
*The difference from GitFlow is that this model doesn't have release branches.*

***Forking workflow***

This strategy is generally used in open-source projects.
Each developer creates their own fork (copy) and they work on changes in separate branches.
Collaboration happens through pull requests.

***Trunk-based Development***

There's a single main branch representing the current state of application.
Integration & deployment practices are continuous for ensuring stability.

***Release Branching***

This involves creating a separate branch for preparing releases.
Bug fixes & release-specific changes are implemented in the release branch while the main branch remains unaffected.