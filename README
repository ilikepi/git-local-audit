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

## Known issues

* Expects `master` to be the branch into which feature branches are merged
* Output is quite rough
* Code is quite rough
* Documentation is quite rough
