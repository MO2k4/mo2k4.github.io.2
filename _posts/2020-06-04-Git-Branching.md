# Git Branching Strategies
 
The different types of branches we may use are:

**Feature branches**

Feature/Topic branches are often a branch of the origin/develop branch and used to work on features for the next or future releases. They only exist when the feature is under development and will be merged back intoGit Branching Strategies the origin/develop branch.

**Release branches**

These are usually a branch from a point-in-time of the origin/develop where it’s deemed ready for a release. It exists to facilitate a production release. Additional minor work may happen on a release branch before it’s merged into the origin/master and origin/develop.

**Hotfix branches**

Hotfixes generally indicate fixes for issues in production that are discovered post-release. Hotfix branches are create from the origin/master and the changes merged into both origin/develop and origin/master branches.
 
## Git Flow
 
Git Flow comes from the Atlassian family tree. Git Flow describes how feature branches, release branches, master or development branches, and hotfixes are interrelated. Git Flow is useful when you have well defined numbered releases. It’s also extremely handy for large teams building downloadable software, packages and libraries where multiple versions of the project/product may be in production simultaneously. But Git Flow is often considered overkill for smaller software teams and less complicated projects/products.
 
It is not supported by Azure Devops!
 
## GitHub Flow
 
GitHub Flow has it’s origins with the GitHub team. has some of the same elements as Git Flow, such as feature branches. But unlike Git Flow, GitHub Flow combines the master and release branches into a “master” and treats hotfixes just like feature branches. It is better suited to continuous delivery models where changes can be quickly made and easily deployed, sometimes multiple times a day.
 
## Release Flow

Release Flow, a trunk-based development branching, similar to GitHub Flow comes from Microsoft, the Azure DevOps (formerly VSTS) heavily makes use of this strategy – or at least did until recently. In this strategy, the teams do not continuously deploy master to production. Instead, they release the master branch every sprint by creating a branch for each release. When the teams need to bring hotfixes into production, they cherry-pick those changes from master into the release branch. This is a simple strategy that works well particularly for those people familiar with TFVC and prevents the “merge hell” scenario described earlier.

# Code Review / Discussion or why pull request are important

We perform code reviews (CRs) in order to improve code quality and benefit from positive effects on team and company culture. For example:
 
* Committers are motivated by the notion of a set of reviewers who will look over the change request: the committer tends to clean up loose ends, consolidate TODOs, and generally improve the commit. Recognition of coding expertise through peers is a source of pride for many programmers.
* Sharing knowledge helps development teams in several ways:
  * A CR explicitly communicates added/altered/removed functionality to team members who can subsequently build on the work done.
  * The committer may use a technique or algorithm that reviewers can learn from. More generally, code reviews help raise the quality bar across the organization.
  * Reviewers may possess knowledge about programming techniques or the code base that can help improve or consolidate the change; for example, someone else may be concurrently working on a similar feature or fix.
  * Positive interaction and communication strengthens social bonds between team members.
  * Consistency in a code base makes code easier to read and understand, helps prevent bugs, and facilitates collaboration between regular and migratory developer species.
  * Legibility of code fragments is hard to judge for the author whose brain child it is, and easy to judge for a reviewer who does not have the full context. Legible code is more reusable, bug-free, and future-proof.
