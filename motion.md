# Motions

* Flip selection, move cursor to other end: `o` _in visual mode_

## in line

* `<left>`, `h`/`<down>`, `j`/`<up>`, `k`/`<right>` ,`l`
* move `b`ackwards, for`w`ard, to the `e`nd of a word forward, to the end of a word backward (`ge`)
* move `B`ackwards,`<S-left>`, for`W`ard, `<S-Right>`, forward to the `E`nd of a WORD, backward to the end of a WORD (`gE`)
* jump to begin of next/prev line `+`/`-`
* move to given column `g|`
* jump le`F`t, right (`f`) to a char, or until lef`t` , right (`t`) it in the line
  * repeat this: `;` / `,`
* jump to begin of line (`<Home>`,`0`), to last non-blank(`g_`) char, to EOL(`$` / `<End>`)
* jump to the first non-blank(`^`) _in normal and visual mode_

### screen line

* jump to begin screen line(`g0`), middle(`gm`), EOsL (`g$`)
* screen line up/down: `gk`/`gj`

## window

* jump to the top(`H`), `M`iddle, bottom (`L`) line of the window
* move the actual line to the top(`zt`), center(`zz`), bottom(`zb`) line of the window _in normal mode_

## matching char, search

* jump to the next/actual maching char ({['<"">']}) _in normal mode_
* `<n>%` jumps to nth percent of the file _in normal and visual mode_
* jump from inside the opening `[(`/`[{`, closing `])`/`]}` parenthesis/brace
* jump the prev.(`#`)/next(`*`) occurence the word under the cursor
* search forward(`/`), backward(`?`), repeat search forward(`n`), backward(`N`)
  * repeat search forward(`gn`), backward(`gN`) _in visual mode_
* move forward/backward on jump-list `g<`/`g>` _in normal and visual mode_
  * in vim this is <^-i>/<^-o>
  * in vis there is no change jump-list

## file

* move to the end (`G`), to the beginning (`gg`) of the file
* move the given line: `gg`/`G` _in normal mode_

## structure _in normal mode_

* jump sentence backward `(`, forward `)`, jump paragraph backward `{`, forward `}`.

## scroll

* half pages: `<S-PgDn>`/`<S-PgUp>`
* pages `<PgDn>`, `<^-b>`/`<PgUp>`, `<^-f>`
* window lines: `<^-e>`/`<^-y>` _in normal mode_
  * at MacOs <^-y> acts as <^-z>, suspends the editor

## misc

* go absolute byte position(`go`), move count bytes left(`gH`) / right(`gL`), next/prev Unicode char `gh`/`gl` _in normal and visual mode_
* `g8`/`ga` show code of the actual character _in normal mode_
* The next search match in backward/forward direction: `gN`/`gn` _in visual and operator-pending mode_
