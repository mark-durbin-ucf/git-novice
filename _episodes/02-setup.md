---
title: Setting Up Git
teaching: 5
exercises: 0
questions:
- "How do I get set up to use Git?"
objectives:
- "Configure `git` the first time it is used on a computer."
- "Understand the meaning of the `--global` configuration flag."
keypoints:
-   "Use `git config` with the `--global` option to configure a user name, email address, editor, and other preferences once per machine."
---

When we use Git on a new computer for the first time,
we need to configure a few things:

*   our name and email address,
*   what our preferred text editor is,
*   and that we want to use these settings globally (i.e. for every project).

On a command line, Git commands are written as `git verb options`,
where `verb` is what we actually want to do and `options` is additional optional information which may be needed for the `verb`. Here is how a user named John Smith might configure Git:

~~~
$ git config --global user.name "John Smith"
$ git config --global user.email "john.smith@example.com"
~~~
{: .language-bash}

Please use your own name and email address instead of Johns's. This user name and email will be associated with your Git activity,
which means that any changes pushed to
[GitHub](https://github.com/),
[BitBucket](https://bitbucket.org/),
[GitLab](https://gitlab.com/) or
another Git host server
after this lesson will include this information.

For this lesson, we will be using [GitHub](https://github.com/) and so the email address used should be the same as the one you will use when setting up your GitHub account. If you are concerned about privacy, please review [GitHub's instructions for keeping your email address private][git-privacy].


> ## Line Endings
>
> As with other keys, when you hit <kbd>Enter</kbd> or <kbd>↵</kbd> or on Macs, <kbd>Return</kbd> on your keyboard,
> your computer encodes this input as a character.
> Different operating systems use different character(s) to represent the end of a line.
> (You may also hear these referred to as newlines or line breaks.)
> Because Git uses these characters to compare files,
> it may cause unexpected issues when editing a file on different machines. 
> Though it is beyond the scope of this lesson, you can read more about this issue 
> [in the Pro Git book](https://www.git-scm.com/book/en/v2/Customizing-Git-Git-Configuration#_core_autocrlf).
>
> You can change the way Git recognizes and encodes line endings
> using the `core.autocrlf` command to `git config`.
> The following settings are recommended:
>
> On macOS and Linux:
>
> ~~~
> $ git config --global core.autocrlf input
> ~~~
> {: .language-bash}
>
> And on Windows:
>
> ~~~
> $ git config --global core.autocrlf false
> ~~~
> {: .language-bash}
> 
{: .callout}

If you have a favorite text editor, you can change the configuration to use it, following the table below. For today's workshop, we will use the Nano text editor.

| Editor             | Configuration command                            |
|:-------------------|:-------------------------------------------------|
| Atom | `$ git config --global core.editor "atom --wait"`|
| nano               | `$ git config --global core.editor "nano -w"`    |
| BBEdit (Mac, with command line tools) | `$ git config --global core.editor "bbedit -w"`    |
| Sublime Text (Mac) | `$ git config --global core.editor "/Applications/Sublime\ Text.app/Contents/SharedSupport/bin/subl -n -w"` |
| Sublime Text (Win, 32-bit install) | `$ git config --global core.editor "'c:/program files (x86)/sublime text 3/sublime_text.exe' -w"` |
| Sublime Text (Win, 64-bit install) | `$ git config --global core.editor "'c:/program files/sublime text 3/sublime_text.exe' -w"` |
| Notepad (Win)    | `$ git config --global core.editor "c:/Windows/System32/notepad.exe"`|
| Notepad++ (Win, 32-bit install)    | `$ git config --global core.editor "'c:/program files (x86)/Notepad++/notepad++.exe' -multiInst -notabbar -nosession -noPlugin"`|
| Notepad++ (Win, 64-bit install)    | `$ git config --global core.editor "'c:/program files/Notepad++/notepad++.exe' -multiInst -notabbar -nosession -noPlugin"`|
| Kate (Linux)       | `$ git config --global core.editor "kate"`       |
| Gedit (Linux)      | `$ git config --global core.editor "gedit --wait --new-window"`   |
| Scratch (Linux)       | `$ git config --global core.editor "scratch-text-editor"`  |
| Emacs              | `$ git config --global core.editor "emacs"`   |
| Vim                | `$ git config --global core.editor "vim"`   |
| VS Code                | `$ git config --global core.editor "code --wait"`   |

It is possible to reconfigure the text editor for Git whenever you want to change it.

> ## Exiting Vim
>
> Vim can be confusing and intimidating for new users. To exit without saving changes, press <kbd>Esc</kbd> then type `:q!` and hit <kbd>Enter</kbd> or <kbd>↵</kbd> or on Macs, <kbd>Return</kbd>.
> To save your changes and quit, press <kbd>Esc</kbd> then type `:wq` and hit <kbd>Enter</kbd> or <kbd>↵</kbd> or on Macs, <kbd>Return</kbd>.  You do not need to be a Shell power user or Vim expert to complete this workshop; all Vim commands will be provided for you.
{: .callout}

Git (2.28+) allows configuration of the name of the branch created when you
initialize any new repository.  We are going to change the default branch name to `main`. 

~~~
$ git config --global init.defaultBranch main
~~~
{: .language-bash}

> ## Default Git branch naming
>
> Source file changes are associated with a "branch." 
> For new learners in this lesson, it's enough to know that branches exist, and this lesson uses one branch.  
> By default, Git will create a branch called `master` 
> when you create a new repository with `git init` (as explained in the next Episode). This term evokes 
> the racist practice of human slavery and the 
> [software development community](https://github.com/github/renaming)  has moved to adopt 
> more inclusive language. 
> 
> In 2020, most Git code hosting services transitioned to using `main` as the default 
> branch. As an example, any new repository that is opened in GitHub and GitLab default 
> to `main`.  However, Git has not yet made the same change.  As a result, local repositories 
> must be manually configured have the same main branch name as most cloud services.  
> 
> For versions of Git prior to 2.28, the change can be made on an individual repository level.  The 
> command for this is in the next episode.  Note that if this value is unset in your local Git 
> configuration, the `init.defaultBranch` value defaults to `master`.
>
{: .callout}

The five commands we just ran above only need to be run once: the flag `--global` tells Git
to use the settings for every project, in your user account, on this computer.

You can check your settings at any time:

~~~
$ git config --list
~~~
{: .language-bash}

You can change your configuration as many times as you want: use the
same commands to choose another editor or update your email address.


[git-privacy]: https://help.github.com/articles/keeping-your-email-address-private/
