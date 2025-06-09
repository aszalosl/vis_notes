# Command mode

## I/O

* Pipe range: `| cmd`, replace range be result: `< cmd`, send range: `> cmd`
  * `:|fmt`, `:<date`
* run cmd: `! cmd`
  * `:!make`

## Files

* Edit file: `e[!] [args...]`
* Replace range by contents of file: `r [args...]`
  * `:r !<cmd>` in vim is `: < <cmd>` here
* Write range to named file: `w[!] [args...]`
  * `11,23w abc.txt`, `-/Start/,/Stop/w tag.txt`
* Write file and quit: `wq[!] [args...]`
* Change directory: `cd [args...]`

## Windows

* Open file: `open [args...]` (with or without name)
  * in a new window
* Create new window: `new [args...]`, vertically: `vnew [args...]`
* Horizontally split window: `split [args...]`, vertically: `vsplit [args...]`
* Quit the current window: `q[!] [args...]`, exit: `qall[!] [args...]`

## Sam commands

* Append text after range: `a/text/`
  * `:x/^/a/    /` - indent
  * `:x/\n/a/\n/` or `,x/$/a/\n/` - double line-mode
* Change text in range: `c/text/`
  * `:x/([0-9]+) ([a-z ]+)/c/\2 \1/`
  * `:,x/$/a/\n/` - double line-mode
* Delete text in range: `d`
  * `:x/^    /d` - outdent region
  *
* Insert text before range: `i/text/`
* Create selection covering range: `p`
  * `:x/txt/+-p`
* command group: `{`,`}`
  * `:x/Vi/ { i/>/ a/</ }`

## Loop

* Set range and run command on each match: `x/regexp/ command`
  * `,x/vi/ c/>&</`
* As `x` but select unmatched text: `y/regexp/ command`
* If range contains regexp, run command: `g/regexp/ command`
* If range does not contain regexp, run command: `v/regexp/ command`
* Substitute: `s/regexp/text/` doesn't work, use x+c
* Run command on files whose name matches: `X/regexp/ command`
  * `X q` - close all windows but unsaved files
  * `X0i/* common comment*/\n`
  * `X x/pattern/c/replacement/` - replace in all opened files
  * `X/.md/$i/# Tags: /` - insert text at the end of all markdown files
* As `X` but select unmatched files: `Y/regexp/ command`

## Map

* key binding: `map[!] [args...]`
  * `:map <mode> <lhs> <rhs>`
  * `map insert <C-s> <Escape>:w<Enter>`
* As `map` but window local: `map-window[!] [args...]`
* Unmap key binding: `:unmap <mode> <lhs>`
* As `unmap` but window local: `unmap-window [args...]`
* Map keyboard layout `:langmap <locale-keys> <latin-keys>`
  * for Russian, Greek keyboards

## Misc

* older, newer text state: `earlier [args...]`, `later [args...]`
  * `earlier 30s`, `earlier 2m`, `earlier 3h`, `earlier 5d`
* set [option](options.md) `set [args]`
* help `:help`, `<F1>`
* `p` - create a selection covering range, enter into visual mode
  * `:1,10p`
* we can use [registers](register.md) in command line:
  * `yiw` and next`:x/<^-r>"/c/pattern/`
  * there is no default search term as in vim: _:%s//pattern/_
* `<up>` to open the command window with the previous commands
