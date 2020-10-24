# scoop-bucket

[Scoop](http://scoop.sh) is a command-line package manager for Windows. This repository defines a bucket that contains packages for installing [Red](www.red-lang.org) using Scoop.

## Install

* Install [Scoop](http://scoop.sh)
* Add the bucket: `scoop bucket add red http://github.com/red/scoop-bucket.git`
* Update scoop: `scoop update`
* Install red:
    + stable: `scoop install red`
    + latest: `scoop install red-latest`
    
The specified version of the red executable will be downloaded to the scoop install location, and a shim for red.exe is added to the user Path.

## Switching between stable and latest build

Both red packages may be installed concurrently, but they both use `red.exe` for the shim name. The last package installed will take precidence. The `reset` command can be used to repair shims for the inactive package.

* To switch packages:
    + `scoop reset red`
    + `scoop reset red-latest`

## Updating red-latest

The red-latest package refers to the automated build of the red 'master' branch. Scoop does not detect when it has changed. In order to update it, you must use the `-f` (force) flag.

* `scoop update red-latest -f`
