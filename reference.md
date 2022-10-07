---
layout: reference
---

## Git Cheatsheets for Quick Reference

*   Printable Git cheatsheets in several languages are [available here](https://github.github.com/training-kit/) ([English version](https://github.github.com/training-kit/downloads/github-git-cheat-sheet.pdf)). More material is available from the [GitHub training website](http://try.github.io/).
*   An [interactive one-page visualisation](http://ndpsoftware.com/git-cheatsheet.html)
    about the relationships between workspace, staging area, local repository, upstream repository, and the commands associated with each (with explanations).
*   Both resources are also available in other languages (e.g. Spanish, French, and more).
* "[Happy Git and GitHub for the useR](http://happygitwithr.com)" is an accessible, free online book by Jenny Bryan on how to setup and use Git and GitHub with specific references on the integration of Git with RStudio and working with Git in R.
* [Open Scientific Code using Git and GitHub](https://open-source-for-researchers.github.io/open-source-workshop/) - A collection of explanations and short practical exercises to help researchers learn more about version control and open source software.

## Glossary

{:auto_ids}
add
:   To stage changes that you wish to commit. You can commit all the files that have been modified since your last commit, or just one. The `git add` command is used to stage changes you wish to commit. [View documentation for git add command](https://git-scm.com/docs/git-add)

branch
:   A branch in Git is a lightweight movable pointer to a commit. While working on a project, collaborators may make numerous branches to separate workflows such as feature development or bug fixes. The `git branch` command is used to create new branches. [View documentation for git branch command](https://git-scm.com/docs/git-branch)

changeset
:   A group of changes to one or more files that are or will be added
    to a single [commit](#commit) in a [version control](#version-control)
    [repository](#repository).
    
checkout
:   To load the project state at a specific point in its history, such as a [branch](#branch) or [commit](#commit). [View documentation for git checkout command](https://git-scm.com/docs/git-checkout)

commit
:   To record the current state of a set of files (a [changeset](#changeset))
    in a [version control](#version-control) [repository](#repository). As a noun,
    the result of committing, i.e. a recorded changeset in a repository.
    If a commit contains changes to multiple files,
    all of the changes are recorded together. The `git commit` command is used to create a commit.
    [View documentation for git commit command](https://git-scm.com/docs/git-commit)

conflict
:   A change made by one user of a [version control system](#version-control)
    that is incompatible with changes made by other users.
    Helping users [resolve](#resolve) conflicts
    is one of version control's major tasks.

HTTP
:   The Hypertext Transfer [Protocol](#protocol) used for sharing web pages and other data
    on the World Wide Web.

merge
:   (a repository): To reconcile two sets of changes to a
    [repository](#repository). The `git merge` command is used to merge the sets of changes. [View documentation for git merge command](https://git-scm.com/docs/git-merge)

protocol
:   A set of rules that define how one computer communicates with another.
    Common protocols on the Internet include [HTTP](#http) and [SSH](#ssh).

pull
:   To bring in updates from a [remote](#remote) [repository](#repository) repository to a local repository. The `git pull` command is used to pull changes from the associated remote branch to a branch in a local repository. [View documentation for git pull command](https://git-scm.com/docs/git-pull)

push
:   To send updates from a local [repository](#repository) to a remote repository. The `git push` command is used to upload local [repository](#repository) content to a remote repository. [View documentation for git push command](https://git-scm.com/docs/git-push)

remote
:   (of a repository) A version control [repository](#repository) connected to another,
    in such way that both can be kept in sync exchanging [commits](#commit).

repository
:   A storage area where a [version control](#version-control) system
    stores the full history of [commits](#commit) of a project and information
    about who changed what, when.

resolve
:   To eliminate the [conflicts](#conflict) between two or more incompatible changes to a file or set of files
    being managed by a [version control](#version-control) system.

revision
:   A synonym for [commit](#commit).

SHA-1
:   [SHA-1 hashes](https://en.wikipedia.org/wiki/SHA-1) is what Git uses to compute identifiers, including for commits.
    To compute these, Git uses not only the actual change of a commit, but also its metadata (such as date, author,
    message), including the identifiers of all commits of preceding changes. This makes Git commit IDs virtually unique.
    I.e., the likelihood that two commits made independently, even of the same change, receive the same ID is exceedingly
    small.

SSH
:   The Secure Shell [protocol](#protocol) used for secure communication between computers.

timestamp
:   A record of when a particular event occurred.

version control
:   A tool for managing changes to a set of files.
    Each set of changes creates a new [commit](#commit) of the files;
    the version control system allows users to recover old commits reliably,
    and helps manage conflicting changes made by different users.
