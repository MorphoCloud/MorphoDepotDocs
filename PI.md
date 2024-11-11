# Instructions for MorphoDepot PIs (repository owners)

These instructions are intended for a PI such as a professor or biology researcher who wants a group of people to work together to segment a microCT or similar 3D volume using the 3D Slicer software.

## Workflow for PI
* Prep work
  * Make sure you and all your segmenters have github accounts set up (make a list of their github usernames).
  * Put your scan in a publicly available URL, such as a public Dropbox link or AWS S3 bucket.
  * Make yourself familiar with the basics of managing a github repository (e.g. [start here](https://github.com/SlicerMorph/Tutorials/tree/main/git-and-github)).  You will use the Github web interface to configure your repository and assign issues, but you will use the MorphoDepot UI in Slicer to access and review pull requests.
  * Be familiar with [the MoprhoDepot segmenter instructions](https://github.com/pieper/MorphoDepotDocs/blob/main/Segmenter.md).  Follow the instructions to install `gh` and SlicerMorphoDepot.
* Create project repository in github per scan (see [this example repository](https://github.com/pieper/MD_E15))  The following are all standard github operations that you can easily get help for with a Google search into the Github docs.
  * The repository must have:
     * A text file called `master_volume` with the url of the data to be segmented
     * A single file with the .ctbl` extension that contains a valid [Slicer discrete color table](https://slicer.readthedocs.io/en/latest/developer_guide/modules/colors.html) defining the anatomy.
  * Set a [branch protect rule](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-protected-branches/managing-a-branch-protection-rule) for the main branch that an approved pull request is required (also probably require that all conversations are resolved)
  * Enable issues for the repository
  * Add the `MorphoDepot` topic ag to the repository (in the repo settings in the About box) so it appears in this list: https://github.com/topics/morphodepot
  * (Optionally disable other features like wiki and projects to make the repositories simpler)
* Define volume to be segmented (e.g. microCT of frog)
  * Create a file named `master_volume` containing the URL of your volume to be segmented
  * Add a [Slicer color table](https://slicer.readthedocs.io/en/latest/developer_guide/modules/colors.html) in `.ctbl` format with the list of segments and colors
* Create github issues for each subtask (e.g. frog legs, spine, head…)
  * Describe what you want to have the segmenter do for this task
  * Copy a link to the issue into an email to the segmenter asking them to add a comment to the issue discussion (github won't let you assign the issue to them unless they have indicated their interest in the issue).
  * Assign issues to segmentors by their github user id so that they will appear on their TODO list when they use SlicerMorphoDepot
* When notified of PRs ready for review, load them into Slicer's MorphoDepotReview module and review
  * Doubleclick PRs to review
  * Use review comments to provide feedback or request changes
  * If PR is good, use the "Approve pull request" button to merge it into the main branch and close PR 
