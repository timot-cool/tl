# sed

- in place:
`-i, --in-place`

- in place with a backup, specifying suffix:
`-i{{SUFFIX}}, --in-place={{SUFFIX}}`

- default: BRE. Doesn't support PCRE. Use ERE instead:
`-E`

- don't print (e.g. there's already a print clause in the command):
`-n`

- search and replace recursively:
`rg -l "{{pattern}}" . | xargs sed -i {{sed_command}}`

- apply a command (e.g. delete, d) to lines between START_PATTERN and END_PATTERN:
`'/{{START_PATTERN}}/,/{{END_PATTERN}}/ {{d}}'`
(if the range exists multiple times, will be applied multiple times)
