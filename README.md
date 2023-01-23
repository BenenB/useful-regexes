# useful-regexes

## Validation

**Email**

`/[\w]+[\.\w]*[\w]+@\w+\.{1}[\w]+\.?[\w]+/`


## Misc

**Find Images with empty or missing alt attributes**

`<img (?:alt="" ?)*(?:(?!alt)[-\d\w]+="[^"]*" ?)*(?:alt="" ?)*/?>`
