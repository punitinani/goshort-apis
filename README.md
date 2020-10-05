# Goshort.in-apis
Api description for goshort.in


1. Create a short url without alias:
Alias is alternate name of short url.By default there will a unique hash generated to url. If you want your custom name then use this query param in request.

GET /api/v1/create?url=type_your_url_here  HTTP/1.1
Host: goshort.in
Content-Type: application/json

Parameter :
url : weblink which you want to make short.
datatype: string
example: https://github.com/


1. Create a short url with alias:
Alias is alternate name of short url.If you want your own custom hash then use this parameter with query string in request.

GET /api/v1/create?url=type_your_url_here&alias=your_custom_name  HTTP/1.1
Host: goshort.in
Content-Type: application/json

Parameter :
url : weblink which you want to make short.
datatype: string
example: https://github.com/

alias: your custom name of random hash.
datatype: contain letters, numbers, and dashes.
example: github, myhash



















