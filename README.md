# git local-audit

Git subcommand for auditing a local repository.

The primary goal of this script is to help ensure nothing of value exists
solely in a local respository.  This is useful when preparing to decommission
a machine or format a storage device.  The script highlights the following
conditions:

* Local branches, merged into `master` or not, that are out of sync with their
  remote tracking branch, or which lack a remote tracking branch entirely
* Local branches fully merged and sync'd (presumably candidates for deletion)
* Stash entries
* Untracked files, including those matched by .gitignore

## Installation

Manually copy the `git-local-audit` script to a location in your `$PATH`.

## Usage

    $ git local-audit
    ### checking unmerged local branches...
    bug_2918_experimental is unmerged and not synced to its remote

    ### checking merged local branches...
    bug_2817_fix_typo is merged and its remote does not exist
    master is merged and synced

    ### checking stash...
    stash@{0}: WIP on bug_2918_experimental: 04888b0 Fix hyperdrive

    ### listing untracked and ignored files...
     M README
    ?? test.sh
    !! .swp

## Known issues

* Expects `master` to be the branch into which feature branches are merged
* Output is quite rough
* Code is quite rough
* Documentation is quite rough

## Copyright

This software is copyright 2015-2016 James Blanding and is made available
under the GNU GPL version 2.  See LICENSE.txt for details.
