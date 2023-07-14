# Brimstone

This Grasshopper plugin retrieves data from Boverket's Klimatdatabas through API or file access, and makes data available in Grasshopper. The plugin is [available on Food4Rhino](https://www.food4rhino.com/en/app/brimstone?lang=en).

## Latest version

Latest version is 0.1.2

## Components

### 0. Fly!

### 1. Get categories

### 2. Get resources

### 3. Get LCA data

### 4. Calculate solid geometry

## Development

* Development is done in the GHPython components in the brimstone_[version].gh file

### Releasing a new version
* Version increments are done globally by updating `scriptcontext.sticky["brimstone_version"]` in the "Brimstone - 0. Fly!" component
* To save a new version of a component, make any changes, and then for each component go to File > Create User Object in Grasshopper
    * Change the sub-category to the current version
    * Unfortunately there is no way of automating this for now
* Make sure that /dist_template/README.md is up to date
* Make sure to push any changes to Git as detailed below
* Place the following files in /dist/brimstone_[version]/ and zip them (the pack_brimstone.py utility can automate this): 
    * .ghuser files for each component
    * brimstone_[version].gh
    * klimatdatabas_[version].json
    * License.txt (can be found in /dist_template/)
    * README.md (can be found in /dist_template/)
* Upload the .zip file to Food4Rhino

### Git usage

* `git add .` to add all changes made
* `git commit -m"chore/fix/feat: short description of commit"` to document
    * Use `chore` for minor changes, `fix` for bug fix, `feat` for new feature
* `git pull` to get updates from server (fix any merge issues)
* `git push` to push to server

### Incrementing version

## Contact

Author: Toivo Säwén, sawen@chalmers.se

## Changelog

### 0.1.2

* "Categories" component now outputs database version retrieved (if available)
* Added optional language input for API component
* Fixed `WebRequests` for use with Rhino 8 WIP
* Moved global plug-in information to new "Fly" component
* New component connects LCA data to solid geometry and calculates 

### 0.1.1

* Fixed bug with energy category
* Allow list access to resources
* Include name in output
* Allow for extracting custom data

### 0.1.0

* Initial version
