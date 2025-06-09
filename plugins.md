# Plugins I use

## Default plugins

### Complete-filename

* complete file path at primary selection location
  * `^-x^-f` in insert mode
* variant: based on `fzf` instead of `vis-complete`

### Complete-word

* complete word at primary selection location using fzf
  * `^-n` in insert mode
* variant: based on `fzf` instead of `vis-menu`

### Digraph

* insert digraphs
  * `^-k` <char1> <char2>
* `vis-digraph` lists the possibilities

### Filetype

* assign filetypes to extensions

### Number-inc-dec
* increment number in dec/hex/oct format
  * `^-a` increment, `^-x` decrement in normal mode

### Textobject-lexer

* defines the `ii` "current lexer token"

## Complete-keyword

* Complete keyword in current file or in an external dictionary
  * `^-p` in insert mode
* A variant using `fzf` instead of `vis-menu`

## [Vis-commentary](https://github.com/lutobler/vis-commentary)

* Toggle comment on the current or selected lines
  * `gcc` in normal mode
  * `gc` in visual(line) mode

## [Vis-ctags](https://github.com/kupospelov/vis-ctags)

* `ctags` lets us jump around our source code using tags and a stack
  * `^-]` jump to tag under cursor
  * `g^-]` select among positions of the same tag
  * `^-t` jump back
* A variant using `fzf` instead `vis-menu`

## [Vis-filetype-settings](https://github.com/jocap/vis-filetype-settings)

* set options automatically depending on filetype

## [Vis-fzf](https://github.com/guillaumeboudon/vis-fzf)

* Go to a given occurrence within the current pwd
  `:rg` command

## [Vis-fzf-browser](https://github.com/peaceant/vis-fzf-browser)

* Simple fuzzy file browser with the power of FZF
* `:fzfbrowser` (`<space>e` for me)

## [Vis-fzf-insert](http://github.com/niplav/vis-fzf-insert)

* Fuzzy Find to Insert Lines in vis
  * In vis, use the command `[[1` to `[[9` to select lines from different files.
  * `[[[` is synonym for `[[1`, `[[(` is synonym for `[[2`.
* Minor error-fix

## [Vis-fzf-mru](https://github.com/peaceant/vis-fzf-mru)

* Use fzf to open the most recently used files in vis.
* `:fzfmru` (`<space>b` for me)


## [Vis-fzf-open](https://git.sr.ht/~mcepl/vis-fzf-open)

* Use fzf to open files in vis.
  * `:fzf` (and `^-g` for me), next `Enter`/`^-s`/`^-v` to open/split
  * `A-j`/`A-k` - preview-down/up, `^-f`/`^-b` - preview-page down/up
  * `?` - toggle-preview, `A-w` - toggle-preview-wrap, `^-z` - clear-screen

## [Vis-goto-file](https://repo.or.cz/vis-goto-file.git)

* Edit the file whose name is under the cursor/selected
  * `gf` in normal/visual mode
  * `^-w^-f`/`^-wf` in normal/visual - in a new window
  * `:find` like `:e`, but search in the _path_
  * `:sfind` like `:split`, but search in _path_
    * default _path_ is `/usr/include/`, but can be setup with `workspaces`
    * the the summary at the git repo
  * `^-o` in normal mode - goto older position in jump list
* They can jump to `file`, `file:123`, `file:/regex/`, or `file#L123` locations.

## [Vis-quickfix](https://repo.or.cz/vis-quickfix.git)

* Quickfix commands, like in vim
* To create an error list:
  * `:cf [errorfile]` - read error-list from a file
  * `:cb` - read error-list from the actual buffer
  * `:cex shell-command` - generate error-list with the command
    * `:grep args...` - `rg --vimgrep ...`
    * `:make [args]...`
* To navigate the list:
  * `:cn [count]` - next error: `A-j`,  `:cp [count]` - prev. error: `A-k`
  * `:cnf [count]` - next file: `A-l`, `:cpf [count]` - prev. file: `A-h`
  * `:cc [count]` - display error? TODO
  * `:cr` - rewind: `A-H`, `:cla` - last error: `A-L`
* To toggle the error window: `:cw` - `^-w^-w`

## [Vis-spellcheck](https://gitlab.com/muhq/vis-spellcheck)

* TODO

## [Vis-sneak](https://github.com/erf/vis-sneak)

* Jump to a location specified by two characters.
  * Type `s{char}{char}` to move to the next char combo.
  * Type `S{char}{char}` to move back.
  * Type `n` or `N` to find the next or prev match, or append a number to the motion.

## [Vis-snippets](https://github.com/rokf/vis-snippets/)

* This is a plugin for vis that adds an ability to replace ranges with pre-defined text
* Need to `:register` the snippets (per syntax)
  * for applying them, select the keyword (visual), and use the `:snip` command (`Tab` for me)
* the expanded text is string, so you need to handle the placeholders

## [Vis-surround](https://repo.or.cz/vis-surround.git)

* Operators for adding/changing/deleting pairs of block delimiters.
* NORMAL mode:
  * [count] `ys` DELIMITER [count] textobject|motion
  * [count] `cs` DELIMITER1 DELIMITER2
  * [count] `ds` DELIMITER

* VISUAL/VISUAL-LINE mode:
  * `S` DELIMITER
  * `C` DELIMITER1 DELIMITER2
  * `D` DELIMITER
