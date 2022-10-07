---
title: Automated Version Control
teaching: 5
exercises: 0
questions:
- "What is version control and why should I use it?"
objectives:
- "Understand the benefits of an automated version control system."
- "Understand the basics of how automated version control systems work."
keypoints:
- "Version control is like an unlimited 'undo'."
- "Version control also allows many people to work in parallel."
---

Version control can keep track of the changes submitted by each collaborator, and when those changes were submitted.
Even if you aren't collaborating with other people,
automated version control is much better than this situation:

!["Piled Higher and Deeper" by Jorge Cham, http://www.phdcomics.com](../fig/phd101212s.png)

"Piled Higher and Deeper" by Jorge Cham, http://www.phdcomics.com

This is a common problem: multiple nearly-identical versions of the same document. Popular word processors have features to help with revisions:
* Microsoft Word's [Track Changes](https://support.office.com/en-us/article/Track-changes-in-Word-197ba630-0f5f-4a8e-9a77-3712475e806a)
* Google Docs' [version history](https://support.google.com/docs/answer/190843?hl=en)
* LibreOffice's [Recording and Displaying Changes](https://help.libreoffice.org/Common/Recording_and_Displaying_Changes)

Version control software Git (which we will be using in today's workshop) enables you to create an initial version of a project (an initial <strong>[commit]({{ page.root }}{% link reference.md %}#commit))</strong>), and then commit changes incrementally as you modify the files in your project. This is not automatic, but something you do intentionally to mark your progress. Git tracks the state of all files in your project (called a <strong>[repository]({{ page.root }}{% link reference.md %}#repository)</strong>) at each commit, and you can view any previous commits whenever you want to see a snapshot of your project at that time (this is called <strong>checking out</strong> a commit).

![Changes Are Saved Sequentially](../fig/play-changes.svg)

Changes tracked by a Git respository are separate from the project files. Unlike a Microsoft Word document, the file itself does not know its own history. The Git respository history is stored inside a directory called `.git` in the folder for your repository. It's best to simply ignore this directory and not make any changes to the files there.

![Different Versions Can be Saved](../fig/versions.svg)

Multiple users can make changes to the same file in your project, but this can cause <strong>merge conflicts</strong> if the same part of the file has been edited by multiple users. More on this later.

![Multiple Versions Can be Merged](../fig/merge.svg)

Git is a powerful tool for tracking changes and developing new features in coding projects. Multiple collaborates can create <strong>branches</strong> to work on a single project simultaneously, and then <strong>merge</strong> the different versions together. This is a standard practice in modern software development. Repositories can be hosted centrally in places like [GitHub](https://github.com) so that collaborators can easily sync changes by <strong>pulling</strong> down the latest commits to their local copy of the repository.

> ## Paper Writing
>
> *   Imagine you drafted an excellent paragraph for a paper you are writing, but later you 
>     select the paragraph and delete it. How would you retrieve the *excellent* version of your conclusion? Is it even possible?
>
> > ## Solution
> >
> > *   Recovering the excellent version is only possible if you created a copy
> >     of the file when that paragraph was still part of your document. <strong>Version control
> >     only tracks what you commit.</strong> If you commit small changes to your files,
> >     and commit often, you will have an extremely detailed history of your changes.
> >     The number of "snapshots" of your work are equal to the number of commits you make.
> >     
> {: .solution}
{: .challenge}
