# VIM cheat sheet
## normal mode - navigation

| Key | Basic Navigation
|:---:|---
| h | &#8592;
| j | &#8595;
| k | &#8593;
| l | &#8594;
| [space] | Move to the right or go to next line if at end of line

| Key | Letter Navigation
|:---:|---
| f + \<char\> | Move to next inline \<char\>
| &#8679; + F + \<char\> | Move to previous inline \<char\>
| t + \<char\> | Move just before the next inline \<char\>
| &#8679; + T +  \<char\> | Move just before the previous inline \<char\>

| Key | Word Navigation
|:---:|---
| w | Go to the start of the next word
| &#8679; + W | Go to the start of the next WORD
| e | Go to the end of the next word
| &#8679; + E | Go to the end of the next WORD
| b | Go to the start of the previous word
| &#8679; + B | Go to the start of the previous WORD

| word / WORD | Example | # of words
|:---:|---|---
| word | Home | 1
| WORD | one-two | 3

| Key | Paragraph Navigation
|:---:|---
| &#8679; `+ {` | Go to the previous paragraph
| &#8679; `+ }` | Go to the next paragraph

| Key | File Navigation
|:---:|---
| gg | Go to start of file
| &#8679; + G | Go to end of file
| \<i\> +  &#8679; + G | Go to start of line \<i\> #1
| :\<i\> | Go to start of line \<i\> #2
| :\<i\> | Go to start of line \<i\>
| &#8679; + $ | Go to end of line
| &#8679; + ^ | Go to start of line (non-WS*)
| 0 | Go to start of line

\* non-whitespace

| Key | History
|:---:|---
| u | Undo
| `ctrl` + r | Redo

| Key | Search
|:---:|---
| /\<search\> | Search(can be regex) and move forworth
| n | Find next
| &#8679; + N | Find previous (backward)
| ?\<search\> | Search and move backwards
| :set incsearch | Incremental search
| :set ignorecase | Ignore case when searching
| :set hlsearch | Highlight search result\'s
| :nohlsearch / :noh | Disable hightligting search result\'s
| d/\<search\> | Delete everything up to first search result
| c/\<search\> | Delete  everything up to first search result + \<insert\>-mode

| Key | Search and replace
|:---:|---
| :s/\<a\>/\<b\> | Replace \<a\> with \<b\> on the current line
| :%s/\<a\>/\<b\> | Replace first occurance of \<a\> with \<b\> on every line
| :%s/\<a\>/\<b\>/gc | Replace all occurances of \<a\> with \<b\> in the file
| :[...]/gci | Flags: global, comfirm, insensitive (case)

__Note:__
When you have your cursor on a bracket/parentesis/... you can press `v + %` to select everything within. You can then continue and search (and replace) withing the selection.

| Key | Delete
|:---:|---
| x | Delete char
| &#8679; + X | Delete char before cursor
| r | Replace char
| &#8679; + R | \<replace\>-mode (overwrite)
| dw | Delete word
| db | Delete previous word
| cw | dw + \<insert\>-mode
| cb | db + \<insert\>-mode
| dd | delete current line
| cc | dd + \<insert\>-mode
| dj | Delete line + line+1

| Key | Delete (special)
|:---:|---
| dt + \<char\> | Delete everything from cursor to \<char\>
| ct + \<char\> | dt + \<char\> + \<insert\>-mode
| di + \<char\> | Delete everything inbetween \<char\>
| ci + \<char\> | di + \<char\> + \<insert\>-mode
| da + \<char\> | Delete everything inbetween \<char\> incl. itself
| ca + \<char\> | Delete everything inbetween \<char\> incl. itself + \<insert\>-mode

| Key | Copy / Paste
|:---:|---
| p | Paste after cursor
| &#8679; + P | Paster before cursor
| yw | Copy word
| yy | Copy line
| y0 | Copy from cursor to start of line
| y + `ctrl` + g | Copy from cursor to last line file
| 10yj | Copy current line and 10 lines beneath it

| Key | General
|:---:|---
| `ctrl` + g | See some general information about the current file in the statusbar

| Key | Macro's
|:---:|---
| q + \<char\> | Register and record macro. Stop recording by hitting `q`
| @ + \<char\> | Execute macro
| @@ | Execute last used macro
