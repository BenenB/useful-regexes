# useful-regexes

**A list of useful regexes I have created for different puropses**

## Validation

**Email**

`/[\w]+[\.\w]*[\w]+@\w+\.{1}[\w]+\.?[\w]+/`

## Parsing

**URL**

`/(?:(?<protocol>https?):\/\/)?(?<host>(?:(?:[\w\d\-_~]+\.)+[\w\d]+)|(?:localhost)){1}(?::(?<port>\d+))?(?<path>\/[\w\d\-_~\.\/]+)?(?:#(?<fragment>[\w\d\-_~]+))?(?:\?(?<query>[\w\d\-_~=\&]+))?/`

## Misc

**Find Images with empty or missing alt attributes**

`/<img (?:alt="" *)*(?:(?!alt)[-\d\w]+="[^"]*" *)*(?:alt="" *)*(?:(?!alt)[-\d\w]+="[^"]*" *)*(?:alt="" *)*\/?>/`
