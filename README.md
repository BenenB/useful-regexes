# useful-regexes

**A list of useful regexes I have created for different puropses**

## Validation

**Email**

`/[\w]+[\.\w]*[\w]+@\w+\.{1}[\w]+\.?[\w]+/`

## Parsing

**URL**

`/(?:(?<protocol>https?):\/\/)?(?<host>(?:(?:[\w\-\~]+\.)+[\w]+)|(?:localhost)){1}(?::(?<port>\d+))?(?<path>\/[\w\-\~\.\/]+)?(?:#(?<fragment>[\w\-\~]+))?(?:\?(?<query>[\w\-\~\=\&]+))?/`

**FILENAME** => may require `(?J)` flag at the beginning

`(?<name>(?:[^\\\/:*?"'<>|\s]+\.(?<type>[^\\\/:*?"'<>|\s]+)|["'][^\\\/:*?"'<>|]+\.(?<type>[^\\\/:*?"'<>|\s]+)["']))`

**FLEXIBLE CLI ARG** => matches `-flag=arg`, `-flag arg` & `-flag= arg`

`-(?<flag>\w+)(?:(?==)=\s*|\s+)(?<arg>\w+)`

## Misc

**Find Images with empty or missing alt attributes**

`/<img (?:alt="" *)*(?:(?!alt)[-\d\w]+="[^"]*" *)*(?:alt="" *)*(?:(?!alt)[-\d\w]+="[^"]*" *)*(?:alt="" *)*\/?>/`
