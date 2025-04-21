# Insert mode

## Mode change

* `<escape>`,`<^-c>` to [normal](normal.md) mode

## Movement

* move cursor to begin of line `<home>`, first non-blank `<^-a>`, EOL `<^-e>`, `<end>`
* move cursor `<up>`/`<down>`/`<left>`/`<right>`
* move cursor WORDS backwards `<S-left>`, forward `<S-right>`

### Scroll

* by line up/down `<^-x><^-e>`/`<^-x><^-y>`
* by half page `<S-PgUp>`/`<S-PgDn>`
* by page `<PgUp>`/`<PgDn>`

## Insert

* tab (or spaces) `<Tab>`/`<^-i>`
* line break `<Enter>`/`<^-m>`/`<^-j>`
* digraph `<^-k>`, Unicode char `<^-v>`
* content of a [register](registers.md) `<^-r>`
* indent/outdent current line `<^-t>`/`<^-d>`
* left align selections `<S-Tab>`

### Complete

* word in file `<^-n>`
  * [local setup](local.md): word from dictionary `<^-p>`
* file name `<^-x><^-f>` - redefined by me

## Delete

* previous char `<Backspace>`, `<^-h>`, next char `<Delete>`, previous WORD `<^-w>`, until the BOL `<^-u>`

## Other

* Suspend the editor `<^-z>`
