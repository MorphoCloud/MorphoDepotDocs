Workflow for PI
* Create project repository in github per scan (we may want to automate this so all repositories are configured the same way by default)
  * Invite all segmenters to the repo
  * set a branch protect rule for the main branch that an approved pull request is required (also probably require that all conversations are resolved)
  * Enable issues for the repository
  * Add the MorphoDepot topic ag to the repository (in the repo settings in the About box) so it appears in this list: https://github.com/topics/morphodepot
  * (We may want to disable other features like wiki and projects to make the repositories simpler)
* Define volume to be segmented (e.g. microCT of frog)
  *  Upload to site for access by URL, which could be in JS2 ceph storage or as a github release asset (although release assets are capped at 2GB)
  * Put the URL in the designated master volume file in project repository
  * Define the segmentation terminology for the specimen
  * Either use uberon or define a subset of terms
* Create github issues for each subtask (e.g. frog legs, spine, head…)
  * * Assign issues to segmentors by their github user id so that they will appear on their TODO list when they use SlicerMorphoDepot
When notified of PRs ready for review, load them into Slicer and review (probably we'll want to have a reviewer mode in SlicerMorphoDepot to facilitate this).
* Use review comments and screenshots to provide feedback or request changes
* When PR is good, merge it into the main branch
* Publish versioned github releases as segmentation progresses
 
