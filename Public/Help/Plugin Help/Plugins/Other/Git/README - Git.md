# Git

A Community Plugin for [Obsidian.md](https://obsidian.md) to manage your vault with Git.

## Documentation

Requirements, installation steps (including setup for mobile), tips and tricks, common issues and more can be found in the [documentation](https://publish.obsidian.md/git-doc).

For mobile users see [Mobile](#mobile) section below.

### TL;DR (not part of the author's documentation, just what I did)
It is recommended to read the plug in documentation but here are some pointers to get you started.
#### Windows
1. Install latest version of Git, use recommended options at minimum
2. Create a GitHub account
3. Create an empty repo for your campaign notes
	1. Note, you may wish to use a private repo for this. If you do, you may encounter credential issues. Refer to the main documentation for help.
4. Press CTRL+P
5. Type 'git: Clone and existing remote repo'
6. Enter the URL of your repo and click on it when it pops up
7. Type Git and click on it when it pops up.
8. Click on the empty highlighted box.
9. In file manager, move all the files back from the file manager to the vaults root folder

To Update your campaign repo, using the CTRL+P menu
1. git: Commit All
2. git: push

## Highlighted Features

-   Automatic vault backup (pull, commit, push) on a schedule.
-   Pull changes from remote repository on Obsidian startup.
-   Manage different repositories via Git submodules (Opt-in in settings) (Desktop only).
-   Stage, commit and diff individual files via the Source Control View. Open it with the `Open Source Control View` command.
-   List your commits and their changed files (like a `git log`) via the History View. Open it with the `Open History View` command.
-   For viewing the detailed history of a file, I strongly recommend you the [Version History Diff](obsidian://show-plugin?id=obsidian-version-history-diff) plugin.

### Source Control View

![Source Control View](https://raw.githubusercontent.com/denolehov/obsidian-git/master/images/source-view.png)

### History View

![History View](https://raw.githubusercontent.com/denolehov/obsidian-git/master/images/history-view.png)

## Available Commands (not exhaustive)

-   Changes
    -   `List changed files`: Lists all changes in a modal
    -   `Open diff view`: Open diff view for the current file
    -   `Stage current file`
    -   `Unstage current file`
-   Commit
    -   `Commit all changes`: Only commits all changes without pushing
    -   `Commit all changes with specific message`: Same as above, but with a custom message
    -   `Commit staged`: Commits only files that have been staged
    -   `Commit staged with specific message`: Same as above, but with a custom message
-   Backup
    -   `Create Backup`: Commits all changes. If "Push on backup" setting is enabled, will also push the commit.
    -   `Create Backup with specific message`: Same as above, but with a custom message
    -   `Create backup and close`: Same as `Create Backup`, but if running on desktop, will close the Obsidian window. Will not exit Obsidian app on mobile.
-   Remote
    -   `Push`
    -   `Pull`
    -   `Edit remotes`
    -   `Remove remote`
    -   `Clone an existing remote repo`: Opens dialog that will prompt for URL and authentication to clone a remote repo
    -   `Open file on GitHub`: Open the file view of the current file on GitHub in a browser window. Note: only works on desktop
    -   `Open file history on GitHub`: Open the file history of the current file on GitHub in a browser window. Note: only works on desktop
-   Local
    -   `Initialize a new repo`
    -   `Create new branch`
    -   `Delete branch`
    -   `CAUTION: Delete repository`
-   Source Control View
    -   `Open source control view`: Opens side pane displaying [Source control view](#sidebar-view)
    -   `Edit .gitignore`
    -   `Add file to .gitignore`: Add current file to .gitignore

## Desktop

## Authentication

Authentication may require additional setup. See more in the [Authentication documentation](https://publish.obsidian.md/git-doc/Authentication)

### Obsidian on Linux

-   ⚠ Snap is not supported.
-   ⚠ Flatpak is not recommended, because it doesn't have access to all system files.

Please use AppImage instead ([Linux installation guide](https://publish.obsidian.md/git-doc/Installation#Linux))

## Mobile

The git implementation on mobile is **very unstable**!

### Restrictions

The mobile version is supported by [isomorphic-git](https://isomorphic-git.org/), which is a re-implementation of Git in JavaScript, because you cannot use native Git on Android or iOS.

-   SSH authentication is not supported ([isomorphic-git issue](https://github.com/isomorphic-git/isomorphic-git/issues/231))
-   Repo size is limited, because of memory restrictions
-   Rebase merge strategy is not supported
-   Submodules are not supported

### Performance on mobile

> [!caution]
> Depending on your device and available free RAM, Obsidian may
>
> -   crash on clone/pull
> -   create buffer overflow errors
> -   run indefinitely.
>
> It's caused by the underlying git implementation on mobile, which is not efficient. I don't know how to fix this. If that's the case for you, I have to admit this plugin won't work for you. So commenting on any issue or creating a new one won't help. I am sorry.

**Setup:** iPad Pro M1 with a [repo](https://github.com/Vinzent03/obsidian-git-stress-test) of 3000 files reduced from [10000 markdown files](https://github.com/Zettelkasten-Method/10000-markdown-files)

The initial clone took 0m25s. After that, the most time consuming part is to check the whole working directory for file changes. On this setup, checking all files for changes to stage takes 03m40s. Other commands like pull, push and commit are very fast (1-5 seconds).

The fastest way to work on mobile if you have a large repo/vault is to stage individual files and only commit staged files.

## Contact

The Line Authoring feature was developed by [GollyTicker](https://github.com/GollyTicker), so any questions may be best answered by him.

If you have any kind of feedback or questions, feel free to reach out via GitHub issues or `vinzent3` on [Obsidian Discord server](https://discord.com/invite/veuWUTm).

This plugin was initial developed by [denolehov](https://github.com/denolehov). Since March 2021, it's me [Vinzent03](https://github.com/Vinzent03) who is developing this plugin. That's why the GitHub repository got moved to my account in July 2024.

If you find this plugin useful and would like to support its development, you can support me on Ko-fi.

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/F1F195IQ5)
