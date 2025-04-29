# Operators

* shift left/right: `<`, `>`
* `y`ank operator
* `c`hange operator (alias `s`)
* `d`elete operator (alias `x`)
* `p`ut text after, before(`P`) the cursor
* `=` format selection
* uppercase/lowercase/switch case: `gU`/`gu`/`g~`
* Join selected lines: `J`, `gJ` without spaces
* use given register for operator: `"`,
  * `"ay`, `"ap`

> we can cancel the previous operator by selecting a new one
(can use operators in operator-pending mode, too)

* missing text formatting (qq,gw,) rot13 (g?), fold (zf), (exists in vim)
* operators works line-wise, `<count>dj` delete whole lines
