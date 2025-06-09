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

* `! shell-command`  Run the command
* `< shell-command` Replace range by stdout of command
  * `0<date` - insert the date at top
  * `1<date` - replace first line with date
 * better to use this than `:!`, as the output is lost in the first case (vim wait for a key-press)
* `> shell-command` Send range to stdin of command
  * `> logger` - add to the log the current line, `:10,20> ./logger` add several lines
  * `> logger` can log the selection if it is consist several lines
  * works silently
* `| shell-command` Pipe range through command
  * `|fmt` - format the selection, `,|fmt` format the whole file
  * `|sort` - sort the lines of the selection
  * `,|jq` - format the whole json file

## Misc

* `,d` - empty the file
