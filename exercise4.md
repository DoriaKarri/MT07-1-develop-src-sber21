## Activities

**1.GET /api/v1/Activities**

**URL** https://fakerestapi.azurewebsites.net/api/v1/Activities/

**Ожидаемый результат:** Получение списка активностей

**Заголовки запроса:** 

User-Agent: PostmanRuntime/7.32.3

Accept: */*

Cache-Control: no-cache

Postman-Token: d6f5a17c-f7c5-436a-831f-9b8a8d9bce6a

Host: fakerestapi.azurewebsites.net

Accept-Encoding: gzip, deflate, br

Connection: keep-alive

**Тело запроса**: нет

**Заголовки ответа:**

Content-Type: application/json; charset=utf-8; v=1.0

Date: Sat, 26 Aug 2023 20:40:31 GMT

Server: Kestrel

Transfer-Encoding: chunked

api-supported-versions: 1.0

**Тело ответа**:

[

  {

​    "id": 1,

​    "title": "Activity 1",

​    "dueDate": "2023-08-26T21:40:31.9799797+00:00",

​    "completed": **false**

  },…

  {

​    "id": 30,

​    "title": "Activity 30",

​    "dueDate": "2023-08-28T02:40:31.9799917+00:00",

​    "completed": **true**

  }

]

**2. POST /api/v1/Activities**

**URL** https://fakerestapi.azurewebsites.net/api/v1/Activities/

**Ожидаемый результат:** Создание списка активностей

**Заголовки запроса:** 

Content-Type: application/json

User-Agent: PostmanRuntime/7.32.3

Accept: */*

Cache-Control: no-cache

Postman-Token: 464f4ed9-49d5-440f-b05b-003bb0626c03

Host: fakerestapi.azurewebsites.net

Accept-Encoding: gzip, deflate, br

Connection: keep-alive

**Тело запроса**: 

{

 "id": *{{activity_id}}*,

 "title": "string",

 "dueDate": "2023-08-25T22:33:31.237Z",

 "completed": **true**

}

**Заголовки ответа:**

Content-Type: application/json; charset=utf-8; v=1.0

Date: Sat, 26 Aug 2023 20:58:24 GMT

Server: Kestrel

Transfer-Encoding: chunked

api-supported-versions: 1.0

**Тело ответа**:

{

  "id": 1,

  "title": "string",

  "dueDate": "2023-08-25T22:33:31.237Z",

  "completed": **true**

}

**3. POST /api/v1/Activities Error**

**URL** https://fakerestapi.azurewebsites.net/api/v1/Activities/

**Ожидаемый результат:** Ошибка при создании списка активностей

**Заголовки запроса:** 

Content-Type: application/json

User-Agent: PostmanRuntime/7.32.3

Accept: */*

Cache-Control: no-cache

Postman-Token: 38a61e75-5542-4589-b499-3b61f30eb3fd

Host: fakerestapi.azurewebsites.net

Accept-Encoding: gzip, deflate, br

Connection: keep-alive

**Тело запроса**: 

{

 "id": bad,

 "title": "string",

 "dueDate": "2023-08-25T22:33:31.237Z",

 "completed": **true**

}

**Заголовки ответа:**

Content-Type: application/problem+json; charset=utf-8

Date: Sat, 26 Aug 2023 21:07:16 GMT

Server: Kestrel

Transfer-Encoding: chunked

**Тело ответа**:

{

  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",

  "title": "One or more validation errors occurred.",

  "status": 400,

  "traceId": "00-41a7481eae64404aaaf95be66f956eb0-65631e22bb2fea4e-00",

  "errors": {

​    "$.id": [

​      "'b' is an invalid start of a value. Path: $.id | LineNumber: 1 | BytePositionInLine: 8."

​    ]

  }

**4. GET /api/v1/Activities/{id}**

**URL** https://fakerestapi.azurewebsites.net/api/v1/Activities/{{activity_id}}

**Ожидаемый результат:** Получение активности по ID

**Заголовки запроса:** 

User-Agent: PostmanRuntime/7.32.3

Accept: */*

Cache-Control: no-cache

Postman-Token: 36220700-e55b-4999-a757-d5b78a77d9de

Host: fakerestapi.azurewebsites.net

Accept-Encoding: gzip, deflate, br

Connection: keep-alive

**Тело запроса**: нет

**Заголовки ответа:**

Content-Type: application/json; charset=utf-8; v=1.0

Date: Sat, 26 Aug 2023 21:12:53 GMT

Server: Kestrel

Transfer-Encoding: chunked

api-supported-versions: 1.0

**Тело ответа**:

{

  "id": 1,

  "title": "Activity 1",

  "dueDate": "2023-08-26T22:12:54.7730353+00:00",

  "completed": **false**

}

**5. GET /api/v1/Activities/{id}** Error

**URL** https://fakerestapi.azurewebsites.net/api/v1/Activities/{{activity_error_id}}

**Ожидаемый результат:** Ошибка при получение активности по ID

**Заголовки запроса:** 

User-Agent: PostmanRuntime/7.32.3

Accept: */*

Cache-Control: no-cache

Postman-Token: 5136ea1e-cc43-4cdd-ad3b-8cf73212404f

Host: fakerestapi.azurewebsites.net

Accept-Encoding: gzip, deflate, br

Connection: keep-alive

**Тело запроса**: нет

**Заголовки ответа:**

Content-Type: application/problem+json; charset=utf-8

Date: Sat, 26 Aug 2023 21:15:53 GMT

Server: Kestrel

Transfer-Encoding: chunked

**Тело ответа**:

{

  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",

  "title": "One or more validation errors occurred.",

  "status": 400,

  "traceId": "00-79177b4d548d0641baef3ee991a6070d-d666aa144642384b-00",

  "errors": {

​    "id": [

​      "The value '111111111111' is not valid."

​    ]

  }

}

**6. PUT /api/v1/Activities/{id}**

**URL** https://fakerestapi.azurewebsites.net/api/v1/Activities/{{activity_id}}

**Ожидаемый результат:** Обновление активности по ID

**Заголовки запроса:** 

Content-Type: application/json

User-Agent: PostmanRuntime/7.32.3

Accept: */*

Cache-Control: no-cache

Postman-Token: 160f0ca9-4f3a-43cb-b96b-8bd0826bdb4e

Host: fakerestapi.azurewebsites.net

Accept-Encoding: gzip, deflate, br

Connection: keep-alive

**Тело запроса**: 

{

 "id": *{{activity_id}}*,

 "title": "string",

 "dueDate": "2023-08-25T11:53:31.312Z",

 "completed": **true**

}

**Заголовки ответа:**

Content-Type: application/json; charset=utf-8; v=1.0

Date: Sat, 26 Aug 2023 21:22:22 GMT

Server: Kestrel

Transfer-Encoding: chunked

api-supported-versions: 1.0

**Тело ответа**:

{

  "id": 1,

  "title": "string",

  "dueDate": "2023-08-25T11:53:31.312Z",

  "completed": **true**

}

**7. PUT /api/v1/Activities/{id} Error**

**URL** https://fakerestapi.azurewebsites.net/api/v1/Activities/{{activity_id}}

**Ожидаемый результат:** Ошибка обновления активности по ID

**Заголовки запроса:** 

Content-Type: application/json

User-Agent: PostmanRuntime/7.32.3

Accept: */*

Cache-Control: no-cache

Postman-Token: c8b2bd0b-75e8-48cc-a823-f0059f3d16a7

Host: fakerestapi.azurewebsites.net

Accept-Encoding: gzip, deflate, br

Connection: keep-alive

**Тело запроса**: 

{

  "id": str,

  "title": "string",

  "dueDate": "2023-08-25T11:53:31.312Z",

  "completed": **true**

}

**Заголовки ответа:**

Content-Type: application/problem+json; charset=utf-8

Date: Sat, 26 Aug 2023 21:25:00 GMT

Server: Kestrel

Transfer-Encoding: chunked

**Тело ответа**:

{

  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",

  "title": "One or more validation errors occurred.",

  "status": 400,

  "traceId": "00-3ba8da876d5cd74c9c9b805ddce2fe2f-3cb0bcdd705fdc48-00",

  "errors": {

​    "$.id": [

​      "'s' is an invalid start of a value. Path: $.id | LineNumber: 1 | BytePositionInLine: 10."

​    ]

  }

}

**8. DELETE /api/v1/Activities/{id}**

**URL** https://fakerestapi.azurewebsites.net/api/v1/Activities/{{activity_id}}

**Ожидаемый результат: **Удаление  активности по ID

**Заголовки запроса:** 

User-Agent: PostmanRuntime/7.32.3

Accept: */*

Cache-Control: no-cache

Postman-Token: b18a6a91-0076-41c1-a914-161600c836e2

Host: fakerestapi.azurewebsites.net

Accept-Encoding: gzip, deflate, br

Connection: keep-alive

**Тело запроса**: нет

**Заголовки ответа:**

Content-Length: 0

Date: Sat, 26 Aug 2023 21:28:14 GMT

Server: Kestrel

api-supported-versions: 1.0

**Тело ответа**: нет

## **Authors**

**9.GET /api/v1/Authors**

**URL** https://fakerestapi.azurewebsites.net/api/v1/Authors

**Ожидаемый результат:**  Получение списка авторов

**Заголовки запроса:** 

User-Agent: PostmanRuntime/7.32.3

Accept: */*

Cache-Control: no-cache

Postman-Token: e5de85f3-f402-4a59-a723-abec62d713d6

Host: fakerestapi.azurewebsites.net

Accept-Encoding: gzip, deflate, br

Connection: keep-alive

**Тело запроса**: нет

**Заголовки ответа:**

Content-Type: application/json; charset=utf-8; v=1.0

Date: Sat, 26 Aug 2023 21:53:50 GMT

Server: Kestrel

Transfer-Encoding: chunked

api-supported-versions: 1.0

**Тело ответа**:

[

  {

​    "id": 1,

​    "idBook": 1,

​    "firstName": "First Name 1",

​    "lastName": "Last Name 1"

  },…

  {

​    "id": 590,

​    "idBook": 200,

​    "firstName": "First Name 590",

​    "lastName": "Last Name 590"

  }

]

**10. POST /api/v1/Authors**

**URL** https://fakerestapi.azurewebsites.net/api/v1/Authors

**Ожидаемый результат:** Создание списка авторов

**Заголовки запроса:** 

Content-Type: application/json

User-Agent: PostmanRuntime/7.32.3

Accept: */*

Cache-Control: no-cache

Postman-Token: 909ae4ec-08e4-4e19-8fc9-0b5fce2bd86f

Host: fakerestapi.azurewebsites.net

Accept-Encoding: gzip, deflate, br

Connection: keep-alive

**Тело запроса**: 

{

 "id": *{{author_id}}*,

 "idBook": *{{book_id}}*,

 "firstName": "string",

 "lastName": "string"

}

**Заголовки ответа:**

Content-Type: application/json; charset=utf-8; v=1.0

Date: Sat, 26 Aug 2023 21:55:58 GMT

Server: Kestrel

Transfer-Encoding: chunked

api-supported-versions: 1.0

**Тело ответа**:

{

  "id": 1,

  "idBook": 1,

  "firstName": "string",

  "lastName": "string"

}

**11. POST /api/v1/Authors Error**

**URL** https://fakerestapi.azurewebsites.net/api/v1/Authors

**Ожидаемый результат:** Ошибка при создании списка авторов

**Заголовки запроса:** 

Content-Type: application/json

User-Agent: PostmanRuntime/7.32.3

Accept: */*

Cache-Control: no-cache

Postman-Token: 93bad6e4-5a13-43ed-8fc0-af5190b43967

Host: fakerestapi.azurewebsites.net

Accept-Encoding: gzip, deflate, br

Connection: keep-alive

**Тело запроса**: 

{<br>
  2,<br>
  "idBook": 0,<br>
  "firstName": "string",<br>
  "lastName": "string"<br>
}<br>

**Заголовки ответа:**

Content-Type: application/problem+json; charset=utf-8

Date: Sat, 26 Aug 2023 21:59:15 GMT

Server: Kestrel

Transfer-Encoding: chunked

**Тело ответа**:

{

"type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",

"title": "One or more validation errors occurred.",

"status": 400,

"traceId": "00-9ace7cb3d7cf5d4393d852e5f14ea11e-56251885ea0dea4f-00",

"errors": {

"$": [

"'2' is an invalid start of a property name. Expected a '\"'. Path: $ | LineNumber: 1 | BytePositionInLine: 2."

]

}

}

}

**12. GET /api/v1/Authors/authors/books/{idBook}**

**URL** https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/{{book_id}}

**Ожидаемый результат:** Получение информации о конкретной книге автора по ID

**Заголовки запроса:** 

User-Agent: PostmanRuntime/7.32.3

Accept: */*

Cache-Control: no-cache

Postman-Token: 52e85905-d3c6-445a-8277-fd2a3d7c76c6

Host: fakerestapi.azurewebsites.net

Accept-Encoding: gzip, deflate, br

Connection: keep-alive

**Тело запроса**: нет

**Заголовки ответа:**

Content-Type: application/json; charset=utf-8; v=1.0

Date: Sat, 26 Aug 2023 22:16:15 GMT

Server: Kestrel

Transfer-Encoding: chunked

api-supported-versions: 1.0

**Тело ответа**:

[

  {

​    "id": 1,

​    "idBook": 1,

​    "firstName": "First Name 1",

​    "lastName": "Last Name 1"

  },

  {

​    "id": 2,

​    "idBook": 1,

​    "firstName": "First Name 2",

​    "lastName": "Last Name 2"

  },

  {

​    "id": 3,

​    "idBook": 1,

​    "firstName": "First Name 3",

​    "lastName": "Last Name 3"

  }

]

**13. GET /api/v1/Authors/authors/books/{idBook} Error**

**URL** https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/{{book_error_id}}

**Ожидаемый результат:** Ошибка при получении информации о конкретной книге автора по ID

**Заголовки запроса:** 

User-Agent: PostmanRuntime/7.32.3

Accept: */*

Cache-Control: no-cache

Postman-Token: 595c7b5b-5eef-4fff-bb62-bbff04d114e6

Host: fakerestapi.azurewebsites.net

Accept-Encoding: gzip, deflate, br

Connection: keep-alive

**Тело запроса**: нет

**Заголовки ответа:**

Content-Type: application/problem+json; charset=utf-8

Date: Sat, 26 Aug 2023 22:18:47 GMT

Server: Kestrel

Transfer-Encoding: chunked

**Тело ответа**:

{

  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",

  "title": "One or more validation errors occurred.",

  "status": 400,

  "traceId": "00-d069d2142938b94ebdc78a6d4ad6796f-913963bcc26c5d49-00",

  "errors": {

​    "idBook": [

​      "The value '9999999999' is not valid."

​    ]

  }

}

**14. GET /api/v1/Authors/{id}**

**URL** https://fakerestapi.azurewebsites.net/api/v1/Authors/{{author_id}}

**Ожидаемый результат:** Получение информации о конкретном авторе по ID 

**Заголовки запроса:** 

User-Agent: PostmanRuntime/7.32.3

Accept: */*

Cache-Control: no-cache

Postman-Token: 407e7139-820c-4df4-a8fd-df9c5eba970f

Host: fakerestapi.azurewebsites.net

Accept-Encoding: gzip, deflate, br

Connection: keep-alive

**Тело запроса**: нет

**Заголовки ответа:**

Content-Type: application/json; charset=utf-8; v=1.0

Date: Sat, 26 Aug 2023 22:29:15 GMT

Server: Kestrel

Transfer-Encoding: chunked

api-supported-versions: 1.0

**Тело ответа**:

{

  "id": 1,

  "idBook": 1,

  "firstName": "First Name 1",

  "lastName": "Last Name 1"

}

**15. GET /api/v1/Authors/{id} Error**

**URL** https://fakerestapi.azurewebsites.net/api/v1/Authors/{{author_error_id }}

**Ожидаемый результат:** Ошибка при получении информации о конкретной книге автора по ID

**Заголовки запроса:** 

User-Agent: PostmanRuntime/7.32.3

Accept: */*

Cache-Control: no-cache

Postman-Token: 0863fa5e-4e5b-4e4d-9257-bac8d1a63ae2

Host: fakerestapi.azurewebsites.net

Accept-Encoding: gzip, deflate, br

Connection: keep-alive

**Тело запроса**: нет

**Заголовки ответа:**

Content-Type: application/problem+json; charset=utf-8

Date: Sat, 26 Aug 2023 22:35:26 GMT

Server: Kestrel

Transfer-Encoding: chunked

**Тело ответа**:

{

  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",

  "title": "One or more validation errors occurred.",

  "status": 400,

  "traceId": "00-fc9e1f987523674993a7b68512ebe6f7-de32791c6385724d-00",

  "errors": {

​    "id": [

​      "The value '5555555555' is not valid."

​    ]

  }

}

**16. PUT ​/api​/v1​/Authors​/{id}**

**URL** https://fakerestapi.azurewebsites.net/api/v1/Authors/{{author_id}}

**Ожидаемый результат:** обновление информации о конкретном авторе по ID

**Заголовки запроса:** 

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: ebeae10c-01fc-4e26-a7b2-e47db08a2842
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**:
{
  "id": {{author_id}},
  "idBook": {{book_id}},
  "firstName": "string",
  "lastName": "string"
}

**Заголовки ответа:**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 27 Aug 2023 07:33:11 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**:

{"id":1,
"idBook":1,
"firstName":"string",
"lastName":"string"}


**17. PUT /api​/v1​/Authors​/{id} Error**

**URL** https://fakerestapi.azurewebsites.net/api/v1/Authors/{{author_id}}

**Ожидаемый результат:** ошибка при обновлении информации о конкретном авторе по ID 

**Заголовки запроса:** 
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: ebeae10c-01fc-4e26-a7b2-e47db08a2842
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**:

{

 "id": h,

 "idBook": {{book_id}},

 "firstName": "string",

 "lastName": "string"

}

**Заголовки ответа:**
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 27 Aug 2023 07:33:11 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**:

{

    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",

    "title": "One or more validation errors occurred.",

    "status": 400,

    "traceId": "00-f11638a093136f46b7ed5475c5f0f080-f0b9ddaa5e260a4b-00",

    "errors": {

        "$": [

            "'0xD0' is an invalid start of a value. 
          Path: $ | LineNumber: 0 | BytePositionInLine: 0."

        ]

    }

}

**18. DELETE/api​/v1​/Authors​/{id}**

**URL** https://fakerestapi.azurewebsites.net/api/v1/Authors/{{author_id}}

**Ожидаемый результат:** удаление информации о конкретном авторе по id

**Заголовки запроса:**
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: ebeae10c-01fc-4e26-a7b2-e47db08a2842
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса:** нет 

**Заголовки ответа:**
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 27 Aug 2023 07:33:11 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа:** нет 

## **Books**

**19. GET ​/api​/v1​/Books**

**URL** https://fakerestapi.azurewebsites.net/api/v1/Books

**Ожидаемый результат:**  Получение информации о книге

**Заголовки запроса:** 
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 876d154b-ee9d-44d2-8cf9-04e69d727852
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**: нет

**Заголовки ответа:**
Response Headers
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 27 Aug 2023 08:56:37 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**:
[
    {
        "id": 1,
        "title": "Book 1",
        "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
        "pageCount": 100,
        "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
        "publishDate": "2023-08-26T08:56:37.2241604+00:00"
    },
    ...
{
        "id": 200,
        "title": "Book 200",
        "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
        "pageCount": 20000,
        "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
        "publishDate": "2023-02-08T08:56:37.227766+00:00"
    }
]

**20. POST /api​/v1​/Books**

**URL** https://fakerestapi.azurewebsites.net/api/v1/Books

**Ожидаемый результат:** создание информации о книге

**Заголовки запроса:** 

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: b7cbdcf6-b45c-4748-a882-6446cb0a6f27
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**: 
{
  "id": {{book_id}},
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-08-25T23:12:50.937Z"
}

**Заголовки ответа:**
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 27 Aug 2023 09:14:21 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**:
{
    "id": 1,
    "title": "string",
    "description": "string",
    "pageCount": 0,
    "excerpt": "string",
    "publishDate": "2023-08-25T23:12:50.937Z"
}

**21. POST /api​/v1​/Books Error**

**URL** https://fakerestapi.azurewebsites.net/api/v1/Books

**Ожидаемый результат:** ошибка при создании информации о книге

**Заголовки запроса:** 

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: b7cbdcf6-b45c-4748-a882-6446cb0a6f27
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**: нет

**Заголовки ответа:**
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 27 Aug 2023 09:14:21 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**:
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-f896d38b3571304c8e948d30c4e6c51e-8245d08f3a2c5541-00",
    "errors": {
        "$": [
            "The JSON value could not be converted to FakeRestAPI.Models.Book. Path: $ | LineNumber: 0 | BytePositionInLine: 1."
        ]
    }
}
       

**22. GET ​/api​/v1​/Books​/{id}**

**URL** https://fakerestapi.azurewebsites.net/api/v1/Books/{{book_id}}

**Ожидаемый результат:** Получение информации о книге по ID 

**Заголовки запроса:** 

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: e98e11c8-161b-45d5-9e43-001eb78ebff5
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**: нет

**Заголовки ответа:**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 27 Aug 2023 10:52:14 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**:

{
    "id": 1,
    "title": "Book 1",
    "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "pageCount": 100,
    "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "publishDate": "2023-08-26T10:52:15.1708108+00:00"
}

**23. GET ​/api​/v1​/Books​/{id} Error**

**URL** https://fakerestapi.azurewebsites.net/api/v1/Books/{{book_error_id}}

**Ожидаемый результат:** ошибка при получении информации о книге по ID

**Заголовки запроса:** 
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 15186fcf-9456-4e98-a59e-74b74dbf4b3c
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**: нет

**Заголовки ответа:**
Content-Type: application/problem+json; charset=utf-8
Date: Sun, 27 Aug 2023 10:59:43 GMT
Server: Kestrel
Transfer-Encoding: chunked

**Тело ответа**:

{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-b943d5be534d1c4bb7b354cb2915ac6b-ad3ca1e160ab8247-00",
    "errors": {
        "id": [
            "The value '{{book_error_id}}' is not valid."
        ]
    }
}

**24. PUT /api​/v1​/Books​/{id}**

**URL** https://fakerestapi.azurewebsites.net/api/v1/Books/{{book_id}}

**Ожидаемый результат:** обновление информации о книге по ID 

**Заголовки запроса:** 

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: f120fd37-e0b8-45be-9993-18988411ef11
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive


**Тело запроса**:

{
  "id": {{book_id}},
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-08-25T23:20:09.115Z"
}

**Заголовки ответа:**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 27 Aug 2023 11:17:32 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**:
{
    "id": 1,
    "title": "string",
    "description": "string",
    "pageCount": 0,
    "excerpt": "string",
    "publishDate": "2023-08-25T23:20:09.115Z"
}

**25. PUT /api​/v1​/Books​/{id} Error**

**URL** https://fakerestapi.azurewebsites.net/api/v1/Books/{{book_id}}

**Ожидаемый результат:** ошибка при обновлении информации о книге по ID

**Заголовки запроса:** 

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 75674d62-2fb1-42e7-af79-69f3e775d9ef
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**:
{

 "id": {{book_id}},

 "title": "string",

 "description": "string",

 "pageCount": 0,

 "excerpt": "string",



}

**Заголовки ответа:**

Content-Type: application/problem+json; charset=utf-8
Date: Sun, 27 Aug 2023 11:26:17 GMT
Server: Kestrel
Transfer-Encoding: chunked

**Тело ответа**:
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-4a8b95d79084f64e9986324b7193ad0d-2bf9790b87618e4b-00",
    "errors": {
        "$": [
            "The JSON object contains a trailing comma at the end which is not supported in this mode. Change the reader options. Path: $ | LineNumber: 14 | BytePositionInLine: 0."
        ]
    }
}

**26. DELETE/api​/v1​/Books​/{id}**

**URL** https://fakerestapi.azurewebsites.net/api/v1/Books/{{book_id}}

**Ожидаемый результат:** удаление информации о книге по ID

**Заголовки запроса:** 

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: aaecde09-cffb-4f76-b74d-130a1e413c8f
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**: нет

**Заголовки ответа:**

Content-Length: 0
Date: Sun, 27 Aug 2023 11:35:26 GMT
Server: Kestrel
api-supported-versions: 1.0

**Тело ответа**: нет

## **CoverPhotos**

**27. GET/api/v1/CoverPhotos**

**URL** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos

**Ожидаемый результат:**  получение списка о фотографии с обложки

**Заголовки запроса:** 

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: b1073d0f-45ed-4785-ad52-0b5750f703c4
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**: нет

**Заголовки ответа:**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 27 Aug 2023 11:42:19 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**:
[
    {
        "id": 1,
        "idBook": 1,
        "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
    },
    ...
    {
        "id": 200,
        "idBook": 200,
        "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 200&w=250&h=350"
    }
]
   
**28. POST /api/v1/CoverPhotos**

**URL** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos

**Ожидаемый результат:** создание списка о фотографии с обложки

**Заголовки запроса:** 

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: f7deb203-b361-4f0a-b9ef-fa9d638ebfd2
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**: 
{
  "id": {{coverphoto_id}},
  "idBook": 0,
  "url": "string"
}

**Заголовки ответа:**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 27 Aug 2023 11:50:39 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**:
  {
    "id": 1,
    "idBook": 0,
    "url": "string"
}

**29. POST /api/v1/CoverPhotos Error**

**URL** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos

**Ожидаемый результат:** ошибка при создании списка о фотографии с обложки

**Заголовки запроса:** 

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: aa2daa90-4f4b-4ffb-b3e2-2ef5b71d0e95
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**: нет

**Заголовки ответа:**

Content-Type: application/problem+json; charset=utf-8
Date: Sun, 27 Aug 2023 11:58:53 GMT
Server: Kestrel
Transfer-Encoding: chunked

**Тело ответа**:

{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-8f374185b6e1a9429bef1a20bd0b6967-0dced800a7c1a042-00",
  "errors": {
  "$": [
  "The JSON value could not be converted to FakeRestAPI.Models.CoverPhoto. Path: $ | LineNumber: 0 | BytePositionInLine: 1."
      ]
   }
}


**30. GET /api/v1/CoverPhotos/books/covers/{idBook}**<br>

**URL** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/{{book_id}}<br>

**Ожидаемый результат:** получение информации о фотографии с обложки по id книги<br>

**Заголовки запроса:**<br>

User-Agent: PostmanRuntime/7.32.3 <br>
Accept: */*<br>
Cache-Control: no-cache<br>
Postman-Token: 49f7eaef-2710-46ac-9fdc-892e06cc382e<br>
Host: fakerestapi.azurewebsites.net<br>
Accept-Encoding: gzip, deflate, br<br>
Connection: keep-alive<br>

**Тело запроса:** нет<br>

**Заголовки ответа:**<br>

Content-Type: application/json; charset=utf-8; v=1.0<br>
Date: Sat, 26 Aug 2023 21:10:10 GMT<br>
Server: Kestrel<br>
Transfer-Encoding: chunked<br>
api-supported-versions: 1.0<br>

**Тело ответа:**<br>

[<br>
    {<br>
        "id": 1,<br>
        "idBook": 1,<br>
        "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"<br>
    }<br>
]<br>

**31. GET /api/v1/CoverPhotos/books/covers/{idBook} Error<br>**

**URL** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/{{book_error_id}}<br>

**Ожидаемый результат:** ошибка при получении информации о фотографии с обложки по id книги<br>

**Заголовки запроса:**<br>

User-Agent: PostmanRuntime/7.32.3<br>
Accept: * / *<br>
Cache-Control: no-cache<br>
Postman-Token: 93818050-ea77-4d37-b179-16aeab4d6968<br>
Host: fakerestapi.azurewebsites.net<br>
Accept-Encoding: gzip, deflate, br<br>
Connection: keep-alive<br>

**Тело запроса:** нет<br>

**Заголовки ответа:**<br>

Content-Type: application/json; charset=utf-8; v=1.0<br>
Date: Sat, 26 Aug 2023 21:43:04 GMT<br>
Server: Kestrel<br>
Transfer-Encoding: chunked<br>
api-supported-versions: 1.0<br>

**Тело ответа:** <br>
{

    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",

    "title": "One or more validation errors occurred.",

    "status": 400,

    "traceId": "00-f9d0cdd3799c594f958df837304c8ed6-d8c402d34a481e4a-00",
    
    "errors": {

        "idBook": [

            "The value '9999999999' is not valid."

        ]

    }

}


**32. GET ​/api​/v1​/CoverPhotos​/{id} <br>**

**URL** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{coverphoto_id}}<br>

**Ожидаемый результат:** получение информации о фотографии с обложки по id<br>

**Заголовки запроса:**<br>

User-Agent: PostmanRuntime/7.32.3<br>
Accept: * / *<br>
Cache-Control: no-cache<br>
Postman-Token: aa247972-5f87-4d7e-8866-3c5bf8493e9f<br>
Host: fakerestapi.azurewebsites.net<br>
Accept-Encoding: gzip, deflate, br<br>
Connection: keep-alive<br>

**Тело запроса:** нет<br>

**Заголовки ответа:**<br>

Content-Type: application/json; charset=utf-8; v=1.0<br>
Date: Sat, 26 Aug 2023 21:51:15 GMT<br>
Server: Kestrel<br>
Transfer-Encoding: chunked<br>
api-supported-versions: 1.0<br>

**Тело ответа:**<br>

{<br>
    "id": 1,<br>
    "idBook": 1,<br>
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"<br>
}<br>

**33. GET ​/api​/v1​/CoverPhotos​/{id} Error<br>**

**URL** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/333<br>

**Ожидаемый результат:** ошибка при получении информации о фотографии с обложки по id<br>

**Заголовки запроса:**<br>

User-Agent: PostmanRuntime/7.32.3<br>
Accept: * / *<br>
Cache-Control: no-cache<br>
Postman-Token: c3b71c2b-e9ec-460e-a07b-cfd15a4aba27<br>
Host: fakerestapi.azurewebsites.net<br>
Accept-Encoding: gzip, deflate, br<br>
Connection: keep-alive<br>

**Тело запроса:** нет<br>

**Заголовки ответа:**<br>

Content-Type: application/problem+json; charset=utf-8; v=1.0<br>
Date: Sat, 26 Aug 2023 21:54:34 GMT<br>
Server: Kestrel<br>
Transfer-Encoding: chunked<br>
api-supported-versions: 1.0<br>

**Тело ответа:**<br>

{<br>
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",<br>
    "title": "Not Found",<br>
    "status": 404,<br>
    "traceId": "00-6e66284c00e5cb469fd96284f2a8a260-31784dc2c1dfcf41-00"<br>
}<br>

**34. PUT ​/api​/v1​/CoverPhotos​/{id} <br>**

**URL** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{coverphoto_id}}<br>

**Ожидаемый результат:** обновление информации о фотографии с обложки по id<br>

**Заголовки запроса:**<br>

Content-Type: application/json<br>
User-Agent: PostmanRuntime/7.32.3<br>
Accept: * / *<br>
Cache-Control: no-cache<br>
Postman-Token: 9bdec9dd-75a3-45a1-883a-86d701ead22c<br>
Host: fakerestapi.azurewebsites.net<br>
Accept-Encoding: gzip, deflate, br<br>
Connection: keep-alive<br>
Content-Length: 51<br>

**Тело запроса:** <br>

{<br>
  "id": {{coverphoto_id}},<br>
  "idBook": {{book_id}},<br>
  "url": "string"<br>
}<br>

**Заголовки ответа:**<br>

Content-Type: application/json; charset=utf-8; v=1.0<br>
Date: Sat, 26 Aug 2023 21:57:51 GMT<br>
Server: Kestrel<br>
Transfer-Encoding: chunked<br>
api-supported-versions: 1.0<br>

**Тело ответа:**<br>

{<br>
    "id": 1,<br>
    "idBook": 1,<br>
    "url": "string"<br>
}<br>

**35. PUT ​/api​/v1​/CoverPhotos​/{id} Error <br>**

**URL** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{coverphoto_id}}<br>

**Ожидаемый результат:** ошибка при обновлении информации о фотографии с обложки по id<br>

**Заголовки запроса:**<br>

Content-Type: application/json<br>
User-Agent: PostmanRuntime/7.32.3<br>
Accept: */*<br>
Cache-Control: no-cache<br>
Postman-Token: fe72cb10-2ad6-4c38-9934-40401dd0f1bf<br>
Host: fakerestapi.azurewebsites.net<br>
Accept-Encoding: gzip, deflate, br<br>
Connection: keep-alive<br>
Content-Length: 51<br>

**Тело запроса:** <br>

{<br>
  "id": a,<br>
  "idBook": {{book_id}},<br>
  "url": "string"<br>
}<br>

**Заголовки ответа:**<br>

Content-Type: application/problem+json; charset=utf-8<br>
Date: Sat, 26 Aug 2023 22:01:31 GMT<br>
Server: Kestrel<br>
Transfer-Encoding: chunked<br>

**Тело ответа:**<br>

{<br>
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",<br>
    "title": "One or more validation errors occurred.",<br>
    "status": 400,<br>
    "traceId": "00-48cedcb2cec6594b93447c8d68533d2d-0fb8d97ca2e02f42-00",<br>
    "errors": {<br>
        "$.id": [<br>
            "'a' is an invalid start of a value. Path: $.id | LineNumber: 1 | BytePositionInLine: 8."<br>
        ]<br>
    }<br>
}<br>

**36. DELETE ​/api​/v1​/CoverPhotos​/{id} <br>**

**URL** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{coverphoto_id}}<br>

**Ожидаемый результат:** удаление информации о фотографии с обложки по id<br>

**Заголовки запроса:**<br>

User-Agent: PostmanRuntime/7.32.3<br>
Accept: */*<br>
Cache-Control: no-cache<br>
Postman-Token: a0927f9f-9a67-4d9e-92d8-8da1b11c5268<br>
Host: fakerestapi.azurewebsites.net<br>
Accept-Encoding: gzip, deflate, br<br>
Connection: keep-alive<br>

**Тело запроса:** нет <br>

**Заголовки ответа:**<br>

Content-Length: 0<br>
Date: Sat, 26 Aug 2023 22:41:20 GMT<br>
Server: Kestrel<br>
api-supported-versions: 1.0<br>

**Тело ответа:** нет <br>

## **Users**

**37. GET ​/api​/v1​/Users <br>**

**URL** https://fakerestapi.azurewebsites.net/api/v1/Users<br>

**Ожидаемый результат:** получение списка пользователей<br>

**Заголовки запроса:**<br>

User-Agent: PostmanRuntime/7.32.3<br>
Accept: * / *<br>
Cache-Control: no-cache<br>
Postman-Token: 7126a605-0682-4d2e-ac4f-d45f9bba9946<br>
Host: fakerestapi.azurewebsites.net<br>
Accept-Encoding: gzip, deflate, br<br>
Connection: keep-alive<br>

**Тело запроса:** нет <br>

**Заголовки ответа:**<br>

Content-Type: application/json; charset=utf-8; v=1.0<br>
Date: Sat, 26 Aug 2023 22:43:51 GMT<br>
Server: Kestrel<br>
Transfer-Encoding: chunked<br>
api-supported-versions: 1.0<br>

**Тело ответа:** <br>

[<br>
    {<br>
        "id": 1,<br>
        "userName": "User 1",<br>
        "password": "Password1"<br>
    },<br>
    ...<br>
    {<br>
        "id": 10,<br>
        "userName": "User 10",<br>
        "password": "Password10"<br>
    }<br>
]<br>

**38. POST /api​/v1​/Users** <br>**

**URL** https://fakerestapi.azurewebsites.net/api/v1/Users<br>

**Ожидаемый результат:** создание нового пользователя<br>

**Заголовки запроса:**<br>

Content-Type: application/json<br>
User-Agent: PostmanRuntime/7.32.3<br>
Accept: * / *<br>
Cache-Control: no-cache<br>
Postman-Token: 0b61171a-41c3-468f-8d56-c5df47ce927d<br>
Host: fakerestapi.azurewebsites.net<br>
Accept-Encoding: gzip, deflate, br<br>
Connection: keep-alive<br>
Content-Length: 66<br>

**Тело запроса:** <br>

{<br>
 "id": 1,<br>
 "userName": "test",<br>
 "password": "test"<br>
}<br>

**Заголовки ответа:**<br>

Content-Type: application/json; charset=utf-8; v=1.0<br>
Date: Sat, 26 Aug 2023 22:49:53 GMT<br>
Server: Kestrel<br>
Transfer-Encoding: chunked<br>
api-supported-versions: 1.0<br>

**Тело ответа:** <br>

{<br>
    "id": 1,<br>
    "userName": "test",<br>
    "password": "test"<br>
}<br>

**39. POST ​/api​/v1​/Users Error<br>**

**URL** https://fakerestapi.azurewebsites.net/api/v1/Users<br>

**Ожидаемый результат:** Ошибка при создании нового пользователя<br>

**Заголовки запроса:**<br>

Content-Type: application/json<br>
User-Agent: PostmanRuntime/7.32.3<br>
Accept: * / *<br>
Cache-Control: no-cache<br>
Postman-Token: 7153229a-1361-4de4-a68c-ebb9ef3b8963<br>
Host: fakerestapi.azurewebsites.net<br>
Accept-Encoding: gzip, deflate, br<br>
Connection: keep-alive<br>
Content-Length: 2<br>

**Тело запроса:** нет <br>

**Заголовки ответа:**<br>

Content-Type: application/problem+json; charset=utf-8<br>
Date: Sat, 26 Aug 2023 22:53:52 GMT<br>
Server: Kestrel<br>
Transfer-Encoding: chunked<br>

**Тело ответа:** <br>

{<br>
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",<br>
    "title": "One or more validation errors occurred.",<br>
    "status": 400,<br>
    "traceId": "00-2e9bd73711be234ab47614b95714c5aa-95734dc399ecfb4e-00",<br>
    "errors": {<br>
        "$": [<br>
            "The JSON value could not be converted to FakeRestAPI.Models.User. Path: $ | LineNumber: 0 | BytePositionInLine: 1."<br>
        ]<br>
    }<br>
}<br>

**40. GET​/api​/v1​/Users​/{id} <br>**

**URL** https://fakerestapi.azurewebsites.net/api/v1/Users/{{user_id}}<br>

**Ожидаемый результат:** получение информации о пользователе по id<br>

**Заголовки запроса:**<br>

User-Agent: PostmanRuntime/7.32.3<br>
Accept: * / *<br>
Cache-Control: no-cache<br>
Postman-Token: 57b889ad-9aa2-49c3-a823-5ad99bce5410<br>
Host: fakerestapi.azurewebsites.net<br>
Accept-Encoding: gzip, deflate, br<br>
Connection: keep-alive<br>

**Тело запроса:** нет <br>

**Заголовки ответа:**<br>

Content-Type: application/json; charset=utf-8; v=1.0<br>
Date: Sat, 26 Aug 2023 22:57:06 GMT<br>
Server: Kestrel<br>
Transfer-Encoding: chunked<br>
api-supported-versions: 1.0<br>

**Тело ответа:** <br>

{<br>
    "id": 1,<br>
    "userName": "User 1",<br>
    "password": "Password1"<br>
}<br>

**41. GET ​/api​/v1​/Users​/{id} Error<br>**

**URL** https://fakerestapi.azurewebsites.net/api/v1/Users/11<br>

**Ожидаемый результат:** ошибка при получении информации о пользователе по id<br>

**Заголовки запроса:**<br>

User-Agent: PostmanRuntime/7.32.3<br>
Accept: * / *<br>
Cache-Control: no-cache<br>
Postman-Token: ec421c0a-8642-45de-8b84-28fe9b373a8c<br>
Host: fakerestapi.azurewebsites.net<br>
Accept-Encoding: gzip, deflate, br<br>
Connection: keep-alive<br>

**Тело запроса:** нет <br>

**Заголовки ответа:**<br>

Content-Type: application/problem+json; charset=utf-8; v=1.0<br>
Date: Sat, 26 Aug 2023 23:01:23 GMT<br>
Server: Kestrel<br>
Transfer-Encoding: chunked<br>
api-supported-versions: 1.0<br>

**Тело ответа:** <br>

{<br>
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",<br>
    "title": "Not Found",<br>
    "status": 404,<br>
    "traceId": "00-1b632dfe2aba1e4b954c0e36dcac82fc-9e4b0225a325d946-00"<br>
}<br>

**42. PUT ​/api​/v1​/Users​/{id} <br>**

**URL** https://fakerestapi.azurewebsites.net/api/v1/Users/1{{user_id}}<br>

**Ожидаемый результат:** успешное обновление информации о пользователе по id<br>

**Заголовки запроса:**<br>

Content-Type: application/json<br>
User-Agent: PostmanRuntime/7.32.3<br>
Accept: * / *<br>
Cache-Control: no-cache<br>
Postman-Token: 8052e2ee-840a-4a57-b87f-ff4558213df2<br>
Host: fakerestapi.azurewebsites.net<br>
Accept-Encoding: gzip, deflate, br<br>
Connection: keep-alive<br>
Content-Length: 65<br>

**Тело запроса:**  <br>

{<br>
  "id": {{user_id}},<br>
  "userName": "string",<br>
  "password": "string"<br>
}<br>

**Заголовки ответа:**<br>

Content-Type: application/json; charset=utf-8; v=1.0<br>
Date: Sat, 26 Aug 2023 23:04:36 GMT<br>
Server: Kestrel<br>
Transfer-Encoding: chunked<br>
api-supported-versions: 1.0<br>

**Тело ответа:** <br>

{<br>
    "id": 1,<br>
    "userName": "string",<br>
    "password": "string"<br>
}<br>

**43. PUT /api​/v1​/Users​/{id} Error<br>**

**URL** https://fakerestapi.azurewebsites.net/api/v1/Users/{{user_id}}<br>

**Ожидаемый результат:** ошибка при обновлении информации о пользователе по id<br>

**Заголовки запроса:**<br>

Content-Type: application/json<br>
User-Agent: PostmanRuntime/7.32.3<br>
Accept: * / *<br>
Cache-Control: no-cache<br>
Postman-Token: 2b677910-92a7-4d67-abcd-dbd2b4481dc6<br>
Host: fakerestapi.azurewebsites.net<br>
Accept-Encoding: gzip, deflate, br<br>
Connection: keep-alive<br>
Content-Length: 62<br>

**Тело запроса:**  <br>

{<br>
 "id": 1,<br>
 "userName": "string",<br>
 "password": <br>
}<br>

**Заголовки ответа:**<br>

Content-Type: application/problem+json; charset=utf-8<br>
Date: Sat, 26 Aug 2023 23:08:47 GMT<br>
Server: Kestrel<br>
Transfer-Encoding: chunked<br>

**Тело ответа:** <br>

{<br>
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",<br>
    "title": "One or more validation errors occurred.",<br>
    "status": 400,<br>
    "traceId": "00-b214cb1e51a10b4595f95d825cf2ae13-ba8c34370f5e8e4a-00",<br>
    "errors": {<br>
        ".password": [<br>
            "'}' is an invalid start of a value. Path: .password | LineNumber: 8 | BytePositionInLine: 0."<br>
        ]<br>
    }<br>
}<br>

**44. DELETE ​/api​/v1​/Users​/{id} <br>**

**URL** https://fakerestapi.azurewebsites.net/api/v1/Users/{{user_id}}<br>

**Ожидаемый результат:** успешное удаление пользователя по id<br>

**Заголовки запроса:**<br>

User-Agent: PostmanRuntime/7.32.3<br>
Accept: * / *<br>
Cache-Control: no-cache<br>
Postman-Token: d5343346-0531-40aa-b2dd-e640bd23c42e<br>
Host: fakerestapi.azurewebsites.net<br>
Accept-Encoding: gzip, deflate, br<br>
Connection: keep-alive<br>

**Тело запроса:** нет <br>

**Заголовки ответа:**<br>

Content-Length: 0<br>
Date: Sat, 26 Aug 2023 23:31:32 GMT<br>
Server: Kestrel<br>
api-supported-versions: 1.0<br>

**Тело ответа:** нет <br>
