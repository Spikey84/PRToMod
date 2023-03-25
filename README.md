# PRToMod
This script attempts to convert a pull request from the fa repo into a sim mod. The purpose of this is to allow potential contributers to test and show off their ideas while not requiring it to be remade in PR form if the idea is accpeted.

## How To Use

1. Install Python
https://www.python.org/downloads/ or `sudo apt install python3`

2. Install Github Dependancy
`pip install PyGithub`

3. Generate a Personal Access Token access token from ![here](https://github.com/settings/tokens) and put it into the Token field in the Token.yml file

4. Run main.py

5. Hit enter to automatically fill your token

6. Input your target pull request ID

![Drawing-24 sketchpad(1)](https://user-images.githubusercontent.com/68761514/220483303-0997f8a6-599b-4da8-98f3-d6432ff1ce0d.png)

7. Copy the generated mod out of the script directory and into your FAF mod directory or upload it to the vault



## Limitations
### One change per file
This system entirly overwrites any file it modifies, this means that you cannot overwrite a file twice or play on a diffrent branch than the mod was intended for. For example you cannot play with a PR for FAFBeta on FAFDevelop. Also you cannot play with 2 diffrent PRToMods that work with the same file.
### Removing BP Values
While this script entirly overwrites any bp file it modifies, it is still merging the new file with the old. This means that if you remove a value from a BP file it will default back to the old value. This causes PRs like ![the Bubble Shield PR](https://github.com/FAForever/fa/pull/4434) to not work in mod form. It sees the removal of `Prerequisite = 'Shield',` and defaults to the current base game value of `Prerequisite` which is of course `'Shield'`, thus the mod does not work. 

## Tested PRS
* ![SACU Change](https://github.com/FAForever/fa/pull/4621)
* ![Reclaim Change](https://github.com/FAForever/fa/pull/4705)
* ![A fun sub PR](https://github.com/FAForever/fa/pull/4094)
