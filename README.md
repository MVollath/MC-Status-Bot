# Minecraft Server Status Monitor

## Tableau Version Control Setup

  Our Tableau `.twb` files use relative paths for data sources. To work with this repo, you need to set up a Git filter (one-time setup):

  ### Setup (One-time)

  Run these commands in the repository root:

  ```bash
  git config filter.tableau-paths.clean "sed 's|C:/Users/Maxi/Projects/Minecraft||g'"
  git config filter.tableau-paths.smudge cat

  Then refresh your working files:

  git checkout -- *.twb

  Workflow

  - Work in Tableau as normal - it will save with absolute paths locally
  - When you commit, Git automatically converts to relative paths
  - When you pull, Git keeps the relative paths in your working files
  - Tableau should preserve the relative paths since they work correctly

  Note: The .gitattributes file is already configured to apply this filter to all .twb files.



### TODOs
* [ ] write Readme
