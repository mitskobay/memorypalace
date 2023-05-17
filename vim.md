# VIM

## Starting VIM
- Check if VIM is installed: `vim --version`
- Crash course: `vimtutor`
- Start fresh: `vim`
- Open file: `vim [filename]`
- Open in read mode: `view [filename]`

## Ending VIM
- quit without editing: `:q`
- quit and discard edits: `:q!`
- save and quit: `wq`
- save file: `:w [filename]`

## Basic Navigation
- One step:
-- left `h`, right `l`
-- (real lines) up `k`, down `j`
-- (display lines): up `gk`, down `gj`
- Other real/display line commands:
-- beginning of line: `0`/`g0`
-- beginning of line (nonblank): `^`/`g^`
-- end of line: `$`/`g$`
- Wordwise:
-- forward start `w`, backward start `b`
-- forward end `e`, backward end `ge`
- WORDwise: `W`, `B`, `E`, `gE`
- Linewise: `<line-number>G`
- Jump between `()`,`{}`, `[]`: `%`
- Screenwise:
-- halfscreen up/down (cursor stays): `<C-u>`, `<C-d>`
-- move to top/middle/bottom of screen: `H`, `M`, `L`
- Filewise: beginning `gg`, end `G`

## Advanced Navigation
Idea: use find feature to move around
- linewise search: forward `f{char}`, backward `F{char}`
- use `;` to repeat, `,` to undo
- forward before `t{char}`, backward before `T{char}`
- search command: `/{chars}` execute: `<CR>` cancel: `<Esc>`
- reverse search: `?{chars}`
- next: `n`, previous: `N`
- Repeat last search: `/<CR>`, `?<CR>`
- History (at search prompt): `<Up>`
- Jump back: ``` `` ```
- Move backward/forward through jump history: `<C-o>`, `<C-i>`

## Getting Help
- `<F1>` or `:help`
- Switch windows: `<C-w><C-w>`
- Close window: `:q`
- Choose help topic: `:help [topic]`
