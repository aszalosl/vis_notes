# Text objects

> in Visual and Operator pending mode

* inner block: (),<>, `i(`=`ib`, `i<`, `i[`, `i{`=`iB`
  * outer block with `a`, closing bracket gives the same object
* quoted string, including/excluding quot.marks: _i`_, _i'_, _i"_, / _a'_, _a'_, _a"_
* inside/outside sentence, paragraph: `is`, `ip` / `as`, `ap`
* word/WORD without and with leading+trailing whitespace: `iw`, `iW` / `aw`, `aW`
* block - adjacent lines with the same indentation level: `a<Tab>`=`i<Tab>`
* whole line without ans with leading and trailing whitespace: `il`, `al`
* current lexer token: `ii`
