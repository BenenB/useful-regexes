# useful-regexes

**A rag-tag collection of Regexes, hopefully worth saving for future use**

***__CONTRIBUTIONS WELCOME__***

## Validation
 - **Email**
   - `/^[\w]+[\.\w]*[\w]+@\w+\.{1}[\w]+\.?[\w]+$/`


 - **Filename**
   - Based on characters restricted by windows
   - `/^(?<name>[^\\\/:*?"<>|\s]+)\.(?<type>[^\\\/:*?"<>|\s]+)$/`


## Parsing
 - **URL**
   - `/(?:(?<protocol>https?):\/\/)?(?<host>(?:(?:[\w\-\~]+\.)+[\w]+)|(?:localhost)){1}(?::(?<port>\d+))?(?<path>\/[\w\-\~\.\/]+)?(?:#(?<fragment>[\w\-\~]+))?(?:\?(?<query>[\w\-\~\=\&]+))?/`


 - **Flexible CLI ARGS**
   - Matches cli flags & corresponding arguments, flexible to allow use of equals sign and also allow spaces in arg if enclosed in matching brackets
   - `/-{1,2}(?<flag>\w+)(?:(?:(?=\s*=)\s*=\s*|\s+)(?<br>['"])?(?<arg>(?:(?!\k<br>)(?!-))(?:(?!\k<br>)(?(<br>)[^\n\r]|[^\s]))*)(?(<br>)\k<br>))?/`


## Misc
 - **Find Images with empty or missing alt attributes**
   - `/<img (?:alt="" *)*(?:(?!alt)[-\d\w]+="[^"]*" *)*(?:alt="" *)*(?:(?!alt)[-\d\w]+="[^"]*" *)*(?:alt="" *)*\/?>/`
