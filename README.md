# useful-regexes

## Validation

**Email**

`/[\w]+[\.\w]*[\w]+@\w+\.{1}[\w]+\.?[\w]+/`

## Parsing

**URL**

`/(?:(?<protocol>https?):\/\/)?(?<host>(?:[\w\d-_~]+\.)+[\w\d]+){1}(?::(?<port>\d+))?(?<path>\/[\w\d-_~\.\/]+)?/`

## Misc

**Find Images with empty or missing alt attributes**

`/<img (?:alt="" *)*(?:(?!alt)[-\d\w]+="[^"]*" *)*(?:alt="" *)*(?:(?!alt)[-\d\w]+="[^"]*" *)*(?:alt="" *)*\/?>/`
