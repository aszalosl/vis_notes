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

## Usage

### Normal mode

* If you want to copy the current line into register _k_, you can type: `"kyy`
* Or you can append to a register by using a capital letter: `"Kyy`
* You can then move through the document and paste it elsewhere using: `"kp`
* To paste from system clipboard on Linux: `"+p`
* To paste from "mouse highlight" clipboard on Linux: `"*p`

### Insert mode

* Insert the content of the register _k_: `<^-r>k`

## Macros

* The general purpose registers `"a–"z` can be used to record macros.
* Use one of `"A–"Z` to append to an existing macro.
* `q` starts a recording, `@` plays it back.
* `@@` refers to the most recently recorded macro.
* `@:` repeats the last :-command.
* `@/` is equivalent to `n` in normal mode.
  * These operations always use the first register slot.
