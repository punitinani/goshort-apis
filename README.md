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

Sample request:-
GET /api/v1/create?url=https://web.whatsapp.com/ HTTP/1.1
Host: goshort.in
Content-Type: application/json

Sample response:- 
{
    "hash": "T5h5li",
    "message": "Short Url generated.",
    "ori_url": "https://web.whatsapp.com/",
    "short_url": "goshort.in/T5h5li",
    "status": "success"
}


2. Create a short url with alias:
Alias is alternate name of short url.If you want your own custom hash then use this parameter with query string in request.

GET /api/v1/create?url=type_your_url_here&alias=your_custom_name  HTTP/1.1
Host: goshort.in
Content-Type: application/json

Parameter
url : weblink which you want to make short.
datatype: string
example: https://github.com/

alias: your custom name of random hash.
datatype: contain letters, numbers, and dashes.
example: github, myhash


Sample request:-
GET /api/v1/create?url=https://github.com&alias=GITHUB HTTP/1.1
Host: goshort.in
Content-Type: application/json

Sample response:- 
{
    "hash": "GITHUB",
    "message": "Short Url generated.",
    "ori_url": "https://github.com",
    "short_url": "goshort.in/GITHUB",
    "status": "success"
}


Error:
1. when query parameter url is empty:-

request:
GET /api/v1/create?url= HTTP/1.1
Host: goshort.in
Content-Type: application/json

response:
{
    "message": "Request param url is empty.",
    "status": "error"
}

2. when query param url is wrong:-

request:
GET /api/v1/create?url=https://gi HTTP/1.1
Host: goshort.in
Content-Type: application/json

response:
{
    "message": "Invalid weblink in request param url.",
    "status": "error"
}


3. when query param url is not passed:-

request:
GET /api/v1/create HTTP/1.1
Host: goshort.in
Content-Type: application/json

response:
{
    "message": "Request param url is missing.",
    "status": "error"
}














