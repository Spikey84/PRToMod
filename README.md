# PRToMod
This script attempts to convert a pull request from the fa repo into a sim mod. The purpose of this is to allow potential contributers to test and show off their ideas while not requiring it to be remade in PR form if the idea is accpeted.

## Limitations
### One change per file
This system entirly overwrites any file it modifies, this means that you cannot overwrite a file twice or play on a diffrent branch than the mod was intended for. For example you cannot play with a PR for FAFBeta on FAFDevelop. Also you cannot play with 2 diffrent PRToMods that work with the same file.
### Removing BP Values
While this script entirly overwrites any bp file it modifies, it is still merging the new file with the old. This means that if you remove a value from a BP file it will default back to the old value. This causes PRs like ![the Bubble Shield PR](https://github.com/FAForever/fa/pull/4434) to not work in mod form. It sees the removal of `Prerequisite = 'Shield',` and defaults to the current base game value of `Prerequisite` which is of course `'Shield'`, thus the mod does not work. 

## Tested PRS
* ![SACU Change](https://github.com/FAForever/fa/pull/4621)
* ![Reclaim Change](https://github.com/FAForever/fa/pull/4705)
