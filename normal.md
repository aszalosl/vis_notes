# Normal mode

[Motions](motion.md)

[Selections](selection.md)

[Marks](mark.md)

[Operators](operator.md)

## Mode change

* [insert mode](insert.md)
  * `a`ppend/`A`ppend at EOL, `i`nsert/`I`nsert at first non-blank char
  * `o`pen a new line below /`O`pen a new line above
* Replace mode
  * `r`eplace the char under the cursor
* [visual mode](visual.md)
  * linewise: `V` / char-wise: `v`
  * select current word + switch to visual mode `<^-n>`
  * select from current cursor to the prev./next search term: `gN`/`gn`
* [command mode](command.md): `:`
* [operator-pending mode](pending.md): `c`, `d`, `y`, `<` and `>`

## Vim grammar

* [count][operator](operator.md)[motion](motion.md)/[text-object](text_object,md) or [operator][operator.md](count)<[motion](motion.md)/[text-object](text_object,md)
  * no difference at count-operator orders (in vim the repetition (`.`) differs after this)
    * `2dw` or `d2w`
  * [count1][operator][count2][motion] doesn't work as expected (as product steps in vim)

## Misc

* Repeat command `.`
* delete forward `x`, backward `X`
* `u`ndo, redo: <^-r>, goto older/newer text state `g-`/`g+`
* record macro: `q`, replay it `@`, e.g. `qa...q` and `@a`
* increment/decrement a number: `<^-a>`/`<^-x>`
* suspend editor: `<^-z>`
* help: `<F1>`
* focus next `<^-w>j`/`<^-w>l`, prev. `<^-w>k`/`<^-w>h` window
* split `<^-w>s`, vsplit `<^-w>v`
* restore last selection: `gv`

## Shortcuts

* quit `<^-w>c`
* quit! `ZQ`
* write-quit `ZZ`
* open `<^-w>n`
