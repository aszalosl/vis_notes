# Selections

vis uses selections as core editing primitives.
A selection is a non-empty, directed range with two endpoints called _cursor_ and _anchor_.
A selection can be anchored in which case the anchor remains fixed
 while only the position of the cursor is adjusted.
For non-anchored selections both endpoints are updated.
A singleton selection covers one character on which both cursor and anchor reside.
There always exists a primary selection which remains visible
 (i.e. changes to its position will adjust the viewport).

## [Visual mode](visual.md)

* select the next region matching the current selection: `<C-n>`
  * select all regions matching the current selection: `<^-a>`
* clear current selection, but select next match: `<^-x>`
* remove primary selection: `<^-p>`
* move to the previous/next selection: `<^-u>`, `<^-k>` /  `<^-d>`, `<^-j>`
* complement selections: `~`
* create a new selection at the start/end of every line covered by selection: `I`/`A`
* remove leading and trailing white space from selections: `_`
* left/right-align all selections by inserting spaces: `<Tab>` / `<S-Tab>`
* rotate selections left/right: `-` / `+`
  * select argument-list: `:x/\(.*\)/` or `vi(`
  * adjust selection: `h`, `o`, `l`
  * split arguments: `:y/,/`
  * trim selections: `_`
  * rotate: `-` or `+`
* save current selections in jump list: `gs`

* Remove all but the count selection column: `<^-l>`
* Remove count selection column: `<^-c>`
  * Split words `:x/\w+/`
  * Align columns `<Tab>`
  * Drop first column `<^-c>` or `:g%2`
  * Reduce selections `<Escape>`
  * Move to brace `f}`
  * Align `<S-Tab>`

## [Normal mode](normal.md)

* set current word as selection `<^-n>`
* remove primary selection: `<^-p>`
* move to the previous/next selection: `<^-u>` / `<^-d>`
* Create a new selection on the line below/above `<^-j>` / `<^-k>`
* Create a new selection on the line below/above the last/first selection `<M-C-j>` / `<M-C-k>`
* left/right-align all selections by inserting spaces: `<Tab>` / `<S-Tab>`
* remove leading and trailing white space from selections: `_`
* save current selections in jump list: `gs`
* Reset count or remove all non-primary selections: `<escape>`

* Remove all but the count selection column: `<^-l>`
* Remove count selection column: `<^-c>`

### Differs

* no I/A, no ^-a, no ^-x, no complement, no rotation
