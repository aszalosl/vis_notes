# Vis `:help` reformatted, extended

In this repository I am trying to present the help of the [vis](https://github.com/martanne/vis) text editor
in a different form in order to refresh my knowledge by rereading it from time to time.

## Background

I have been using the vim text editor for almost thirty years.
During this time, this program has undergone many changes, and its built-in [help](https://vimhelp.org)
now stretches toseveral thousand pages.
I have considered switching several times, but I did not want to learn something completely different.
A few years ago, [neovim](https://neovim.io) came up as an option,
but for me the [vimscript](https://neovim.io/doc/user/usr_41.html#_introduction)-[lua](https://neovim.io/doc/user/lua.html) pair setup only complicated the situation.
I had encountered vis before, but during my first, superficial acquaintance, it did not have a great impact on me,
because although I had also heard of [sam](http://sam.cat-v.org), I did not know it in depth.
Finally, a [presentation](https://youtu.be/DJTb0R1_JaM) by the author of vis gave me the impetus to dig a little deeper,
 and as a result, this program became my primary text editor.

## Details

vis is a [modal text editor](https://carlosbecker.com/posts/ed/) in the vi family,
with [normal](normal.md), [insert](insert.md), [visual](visual.md), and [operator-pending](pending.md) modes.
It follows the [verb-noun](https://learnvim.irian.to/basics/vim_grammar)
([operator](operator.md)-[motion](motion.md)) order typical of the family -
in this sense it is not similar to [kakaune](https://kakoune.org) and [helix](https://helix-editor.com).
It is similar to vim in [register](registers.md) handling, but its [marks](mark.md) are significantly different.
This is partly a consequence of the sam inheritance, i.e. we can use multiple cursors and ican have multiple
[selections](selection.md).

Similar to neovim, vis can be extended with Lua [plugins](https://github.com/martanne/vis/wiki/Plugins),
but they are not compatible, so you cannot use neovim plugin in vis. For me, [these](local.md) settings works.

## Links

* [base-16 themes](https://github.com/przmv/base16-vis)
