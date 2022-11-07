# useful-regexes

## Misc

**Find Images with empty or missing alt attributes**

`/<img (alt="" ?)*(?:(?!alt)\w+=".*" ?)*(alt="" ?)*/?>/`
