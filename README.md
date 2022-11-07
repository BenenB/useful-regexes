# useful-regexes

## misc

- Find Images with no/empty alt attributes
  - /<img (alt="" ?)*(?:(?!alt)\w+="\w+" ?)*(alt="" ?)*/?>/
