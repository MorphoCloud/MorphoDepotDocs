# Instructions for MorphoDepot Segmenters

These instructions are intended for a people will work to segment a microCT or similar 3D volume using the 3D Slicer software.

## Prerequsites
* A github account for this work.  *Note: you may want a dedicated account just for your segmentation projects if you are concerned about using your personal github credentials on a cloud machine*
* Familiarity with 3D Slicer's segmenttion tools (See, for example, the [SlicerMorph tutorials](https://github.com/SlicerMorph/Tutorials/blob/main/Segmentation/README.md) and the Slicer documentation at [Slicer.org](https://slicer.org)
* Some basic familiarity with git and github (as [described here](https://github.com/SlicerMorph/Tutorials/tree/main/git-and-github), although you cam mostly accomplish what you need via the web interface).

## Install `gh`
* The `[gh](https://github.com/cli/cli)` tool as [described here](https://github.com/cli/cli?tab=readme-ov-file#installation) and make sure it is in your shell's `PATH` and that you have logged in with your github account.
* Run `gh status` on the command line to confirm it is working

## Installation of MorphoDepot
* During development the MorphoDepot code is available via a github repository (eventually it will be in SlicerMorph or its own extension)
* Clone [this repository](https://github.com/pieper/SlicerMorphoDepot) to your computer (use the green `Code` button
* Start 3D Slicer
* Drag the cloned folder and drop it on 3D Slicer
* Accept the dialog to load the module
* You can find the MorphoDepot module in the SlicerMorph category or by using the Find Module dialog (Control-F, or Command-F on Mac)

## Using MorphoDepot
* The module uses the `gh` command to interact with github on your behalf and work with data in Slicer
* Use the `Refresh` button to get the list of segmentation tasks assigned to you.  These correspond to issues in your PI's repository
* Doubleclick on the issue you want to work on (you will be asked confirm you don't have any unsaved data before loading the issue)
* Once the data has loaded, you will enter the Segment Editor with a blank segmentation.  Use this to complete your task.
* As you work on your segmentation, go back to the MorphoDepot module and use the `Save checkpoint` button to save your work and push the results to github
* If you need to, you can exit slicer (e.g. to shutdown the machine) and reload the issue later to pick up where you left off.
* When you have finished your work, click the "Save and request review" button to create a pull request.  This will open a browser page where you can enter any comments for your PI and create a pull request for the PI to review.
