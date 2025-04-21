# My own settings

## Used plugins

### complete-filename

* using [fzf](https://github.com/junegunn/fzf) insert existing filename into the text
* `<^-x><^-f>` in insert mode - overrides the builtin plugin

### [complete-keyword](https://github.com/jpaulogg/vis-ins-completion)

* based on the content of current file or external dictionary insert a keyword
* redefined to `<^-p>` in insert mode
* this method combine the output of shell commands in the _completeopts_ table
* set `dictfiles` in visrc

### filetype

* builtin plugin
* sets the filetype based on the extension or using command `file`

### [fzf-browser](https://github.com/peaceant/vis-fzf-browser)

* list all files in the current working directory.
* `fzfbrowser` in command mode
* `<space>e` in normal mode

### [fzf-mru](https://github.com/peaceant/vis-fzf-mru)

* builds a list of most recent used files, and you can select among them
* can be set the file containing the file list
* `fzfmru` in command mode
* `<space>b` in normal mode

### [super-shellout](https://github.com/seifferth/vis-super-shellout)

* execute an outer command and read its output
* a bit nicer version of `:<`
* `R` in command mode

### [vis-commentary](https://github.com/lutobler/vis-commentary)

* toggle comment on lines, in many programming languages
* `gc` in visual mode, `gcc` in normal mode

### [vis-ctags](https://github.com/kupospelov/vis-ctags)

* uses tags file generated with [ctags](https://github.com/universal-ctags/ctags)
* `<^-[>` _in normal mode_ to jump to definition
* `g<^-[>` _in normal mode_ to select among definitions
* `<^-t>` _in normal mode_ to jump back

### [vis-editorconfig-options](https://github.com/seifferth/vis-editorconfig)

* uses _.editorconfig_ files to set options
  * calls eco-core.lua
  * needs editorconfig-core - install with luarocks

### [vis-filetype-settings](https://github.com/jocap/vis-filetype-settings)

* we can setup [options](option.md) based on the file-type
* partly concurrent of plugin _vis-editorconfig-options_

### [vis-fzf-open](https://git.sr.ht/~mcepl/vis-fzf-open/)

* opens file in the subtree
* `fzf` in command mode
  * `<Enter>` to open the selected file in current window
  * `<C-s>` to open the selected file in a horizontal split
  * `<C-v>` to open the selected file in a vertical split
* You can pass arguments to fzf, e.g. : `fzf -p !.class`
* `<^-g>` in normal mode
* in preview
  * `<M-j>`/`<M-k>` - next/prev
  * `<^-f>`/`<^-b>` - PgDn/PgUp
  * `?` - toggle preview
  * `<M-w>` - toggle wrap
  * `<^-z>` - clear screen

### [vis-fzf](https://github.com/guillaumeboudon/vis-fzf`)

* uses [ripgrep](https://github.com/BurntSushi/ripgrep/blob/master/GUIDE.md) to find a keyword in the subtree,
  and fzf to select among them
* `rg keyword` in command mode

### [vis-goto-file](https://repo.or.cz/vis-goto-file.git)

* edit the file whose name is under the cursor or is selected.
* They can jump to `file`, `file:123`, `file:/regex/`, or `file#L123` locations.
  * `gf` in normal mode - under the cursor
  * `<^-w><^-f>`/`<^-w>f` in normal mode - under the cursor in a new window
  * `gf` in visual mode - selected name
  * `<^-w><^-f>`/`<^-w>f` in visual mode - selected name in a new window
  * `find` in command mode - searches in path
  * `sfind` in command mode - searches in path, opens in a split
  * `<^-o>` will go back to the previous location in the jump stack.

### [vis-quickfix](https://git.sr.ht/~mcepl/vis-quickfix)

* Go through the errors generated during compiling and fix them,
  original [details](https://vimhelp.org/quickfix.txt.html)
* create errorlist
  * `:cf <errorfile>` / `:cb` / `:cex <shell cmd>` / `:grep <args>` / `:make <args>`
* navigate in errorlist
  * `:cn <cnt>`, `<M-j>`
  * `:cp <cnt>`,  `<M-k>`
  * `:cnf <cnt>`, `<M-l>`
  * `:cnp <cnt>`, `<M-h>`
  * `:cc <cnt>`
  * `:cr`, `<M-H>`
  * `:cla`, `<M-L>`
* toggle errorlist: `:cw`, `<^-w><^-w>`
* needs LuaFileSystem

### [vis-surround](https://repo.or.cz/vis-surround.git)

* Operators for adding/changing/deleting pairs of block delimiters.
* in normal mode:

  * `[count] ys DELIMITER [count] textobject|motion`
  * `[count] cs DELIMITER1 DELIMITER2`
  * `[count] ds DELIMITER`
* in visual/visual-line mode:
  * `S DELIMITER`
  * `C DELIMITER1 DELIMITER2`
  * `D DELIMITER`

### Sometimes

* [spellcheck](https://github.com/fischerling/vis-spellcheck)
* [pairs](https://repo.or.cz/vis-pairs.git)
* [statusline](https://github.com/jpaulogg/vis-statusline)
* [highlight](https://github.com/erf/vis-highlight)

## Shortcuts

### normal mode

* `<space>b` - fzfmru
* `<space>d` - insert date
* `<space>e` - fzfbrowser
* `<space>w` - remove trailing spaces and save file
* `<space>x` - write and quit
* `;;` - next split
* `<^-c>` - insert into system clipboard
* `<^-v>` - paste from system clipboard
* `F3`/`F4` - show/hide white-spaces
* `ZZ` - quit and save if modified

### visual mode

* `<^-c>` - insert into system clipboard
* `<^-v>` - paste from system clipboard

### insert mode

* `<M-^-h>` - delete last mistyped word
