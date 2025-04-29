# Registers

* `a-z` - General purpose registers
* `A-Z` - Append to corresponding general purpose register
* `"` - Unnamed register
* `0` - Yank register
* `&` - Last regex match
* `1`..`9` - 1st..9th sub-expression match
* `_` - /dev/null register
* `+` - System clipboard register, see vis-clipboard(1)
* `*` - Primary clipboard register, see vis-clipboard(1)
* `.` - Last inserted text
* `/` - Last search pattern
* `:` - Last :-command
* `!` - Last shell command given to either <, >, |, or !
* `#` - Register number

* differs from vim: no current filename (%), expression (=), dropped text (~), alternate buffer (#)
 
## Usage

### Normal mode

* If you want to copy the current line into register _k_, you can type: `"kyy`
* Or you can append to a register by using a capital letter: `"Kyy`
* You can then move through the document and paste it elsewhere using: `"kp`
* To paste from system clipboard on Linux: `"+p`
* To paste from "mouse highlight" clipboard on Linux/system clipboard on Mac: `"*p`
* yank 4 words, 5 lines and 3 sentences into register _a_
  * `"ay4w`/`"a4yw`/`4"ayw`, `"a5yy`/`5"ayy`, `"ay3as`/`"a3yas`/`3"ayas`
* delete 7 character left/8 character right into register _b_: `7"bX`/`"b7X`, `8"bx`/`"b8X`
* delete 3 words into register _b_: `3"bdw`/`"b3dw`

### Insert mode

* Insert the content of the register _k_: `<^-r>k`


### Visual mode
* `"ax`, `"ad` - cut the selection into register _a_
* `"ac`, `"as` - cut the selection into register _a_, and go to insert mode
* `"ay` - copy the selection into register _a_ 
* differs from vim: missing __D_ and _Y_, _X_,  _r_, _<Del>_ operators/commands in visual mode


## Macros

* The general purpose registers `"a–"z` can be used to record macros.
* Use one of `"A–"Z` to append to an existing macro.
* `q` starts a recording, `@` plays it back.
* `@@` refers to the most recently recorded macro.
* `@:` repeats the last :-command.
* `@/` is equivalent to `n` in normal mode.
  * These operations always use the first register slot.
* the content of the register can be edited by inserting the text and reloading later, even it contains specific characters
