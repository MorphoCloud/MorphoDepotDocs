# Instructions for MorphoDepot Segmenters

These instructions are intended for a people will work to segment a microCT or similar 3D volume using the 3D Slicer software.

## Prerequsites
* A github account for this work.  *Note: you may want a dedicated account just for your segmentation projects if you are concerned about using your personal github credentials on a cloud machine*
* Familiarity with 3D Slicer's segmentation tools (See, for example, the [SlicerMorph tutorials](https://github.com/SlicerMorph/Tutorials/blob/main/Segmentation/README.md) and the Slicer documentation at [Slicer.org](https://slicer.org)
* Some basic familiarity with git and github (as [described here](https://github.com/SlicerMorph/Tutorials/tree/main/git-and-github), although you cam mostly accomplish what you need via the SlicerMorphoDepot interface).

## Install `gh`
* The [`gh`](https://github.com/cli/cli) tool as [described here](https://github.com/cli/cli?tab=readme-ov-file#installation) and make sure it is in your shell's `PATH` and that you have logged in with your github account.  If you are using a MorphoCloud insance `gh` will be preinstalled.
* If you use Windows, we suggest using the `winget` approach [described here](https://github.com/cli/cli?tab=readme-ov-file#windows).
* If you use Mac, [homebrew](https://brew.sh/) is a good option.
* Use `gh --version` to confirm you have version 2.58.0 or higher.
* Use `gh auth login` to activate your account login, something like this:
```
  $ gh auth login
? Where do you use GitHub? GitHub.com
? What is your preferred protocol for Git operations on this host? HTTPS
? Authenticate Git with your GitHub credentials? Yes
? How would you like to authenticate GitHub CLI? Login with a web browser

! First copy your one-time code: XXXX-XXXX
Press Enter to open github.com in your browser... 
? Authentication complete.
- gh config set -h github.com git_protocol https
? Configured git protocol
! Authentication credentials saved in plain text
? Logged in as <username>
```
* Run `gh status` on the command line to confirm it is working

## Install 3D Slicer
* If needed, get version 5.6.2 or later from [https://download.slicer.org](https://download.slicer.org)

## Installation of MorphoDepot
* During development the MorphoDepot code is available via a github repository (eventually it will be in SlicerMorph or its own extension)
* Clone [this repository](https://github.com/pieper/SlicerMorphoDepot) to your computer (use the green `Code` button.  You can use this command in a terminal window to install it: `gh repo clone pieper/SlicerMorphoDepot`
* Start 3D Slicer
* Drag the cloned folder and drop it on 3D Slicer
* Accept the dialog to load the module
* You can find the MorphoDepot module in the SlicerMorph category or by using the Find Module dialog (Control-F, or Command-F on Mac)

## Accepting issues
* The repository owner will email you with links to issues for you.  Follow those links to github and comment on the issue to indicate interest so the repository owner can assign the issue to you.
* When the issue has been assigned you can access it via the MorphoDepot module.

## Using MorphoDepot
* The module uses the `gh` command to interact with github on your behalf and work with data in Slicer
* Use the `Refresh` button to get the list of segmentation tasks assigned to you.  These correspond to issues in your PI's repository
* Doubleclick on the issue you want to work on (you will be asked confirm you don't have any unsaved data before loading the issue)
* Once the data has loaded, you will enter the Segment Editor with a blank segmentation.  Use this to complete your task.
* Use the terminology provided to you.
* As you work on your segmentation, go back to the MorphoDepot module and use the `Commit and Push` button to save your work and push the results to github. Provide a short description as your `Commit message` and optionally a longer one to describe your work (or to make a note of remaining work that needs to be done). These notes are for yourself.
* When doing work through MorphoDepot, do **NOT** use the regular save functions of Slicer, but use only the `Commit and Push` button to save your work. Regular save will potentially cause data loss. 
* If you need to, you can exit slicer (e.g. to shelve the instance) and reload the issue later to pick up where you left off. If you did the `Commit and Push` prior to closing slicer, you can ignore the message about contents of the scene being unsaved.
* When you have finished your work, click the `Request PR review` button to change your pull request from draft sttaus to ready status.  You need to enter a short description of your work in the text area below the button for your instructor or PI to see. This action will create a trigger to the instructor/PI to review your work. They can merge (accept) it, or may ask you to revise. 
