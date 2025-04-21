# Sam's idioms updated

## Find

* `:/pattern/` find next occurence of the pattern
* `:?pattern?` `:-/pattern/` - find previous occurence of a pattern
* `:$-/pattern/` - last occurence of a pattern
* `:/pattern/+-` select the next line containing the pattern
* `:x/pattern/+-` - grep variant, select all lines containing pattern
* `:-/^$/+,/^$/` - select current paragraph

## delete

* `,x/pattern/ d` - delete all occurences of the pattern
* `,x/pattern/+- d` - delete lines containing pattern

## Indent/outdent

* `:x/^/a/  /` - `<Tab>` doesn't working on MacOs
* `:x/^  /d`

## I/O

* `0<date` - insert the date at top
* `1<date` - replace first line with date
* `|fmt` - format the selection

## Misc

* `,d` - empty the file
