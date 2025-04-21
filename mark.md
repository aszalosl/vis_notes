# Marks

* `m` sets a mark, `M` restores it.
  * `'am` sets the mark a while `'aM` restores it.
  * Use of `m` or `M` without specifying a mark uses the default mark.

* `a-z` general purpose marks
* `'`   default mark
* `^`   last selections

## Visual mode and Normal mode

* Intersect with selections from mark: `&`
* Add selections from mark: `|`
* Subtract selections from mark: `\`
* Save currently active selections to mark: `m`
* Restore selections from mark: `M`
* Use given mark for next action: `'`
