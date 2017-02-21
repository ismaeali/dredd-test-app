# Dredd Tests
## Fail: GET /
### Message
```
headers: Header 'content-type' has value 'application/json' instead of 'application/hal+json'

```

### Request
```
method: GET
uri: /
headers: 
    Content-Type: application/json
    Accept: application/hal+json
    User-Agent: Dredd/2.2.5 (Darwin 15.4.0; x64)

body: 


```

### Expected
```
headers: 
    Content-Type: application/hal+json

body: 
{
  "_links": {
    "self": {
      "href": "ipsum et sed veniam"
    },
    "gists": {
      "href": "sit",
      "templated": true
    }
  }
}
statusCode: 200
bodySchema: {"type":"object","properties":{"_links":{"type":"object","properties":{"self":{"type":"object","properties":{"href":{"type":"string"},"templated":{"type":"boolean"}},"required":["href"]},"gists":{"type":"object","properties":{"href":{"type":"string"},"templated":{"type":"boolean"}},"required":["href"]}},"required":["self","gists"]}},"required":["_links"]}

```

### Actual
```
statusCode: 200
headers: 
    x-powered-by: Express
    content-type: application/json
    link: <http://api.example.com/>;rel="self",<http://api.example.com/gists>;rel="gists"
    content-length: 137
    etag: W/"89-TEoMOpkBn6Op16w2+apkIQ"
    date: Tue, 21 Feb 2017 22:08:31 GMT
    connection: close

body: 
{
  "_links": {
    "self": {
      "href": "/"
    },
    "gists": {
      "href": "/gists?{since}",
      "templated": true
    }
  }
}

```

## Fail: GET /gists/42
### Message
```
headers: Header 'content-type' has value 'application/json' instead of 'application/hal+json'

```

### Request
```
method: GET
uri: /gists/42
headers: 
    Content-Type: application/json
    Accept: application/hal+json
    User-Agent: Dredd/2.2.5 (Darwin 15.4.0; x64)

body: 


```

### Expected
```
headers: 
    Content-Type: application/hal+json

body: 
{
  "created_at": "do reprehenderit ad non in",
  "description": "Excepteur",
  "content": "consectetur in officia ut",
  "id": "velit mollit adipisicing",
  "_links": {
    "self": {
      "href": "laborum ad voluptate pariatur consequat",
      "templated": false
    },
    "star": {
      "href": "ad minim irure d"
    }
  }
}
statusCode: 200
bodySchema: {"type":"object","properties":{"created_at":{"type":"string"},"description":{"type":"string"},"content":{"type":"string"},"id":{"type":"string"},"_links":{"type":"object","properties":{"self":{"type":"object","properties":{"href":{"type":"string"},"templated":{"type":"boolean"}},"required":["href"]},"star":{"type":"object","properties":{"href":{"type":"string"},"templated":{"type":"boolean"}},"required":["href"]}},"required":["self"]}},"required":["created_at","description","content","id","_links"]}

```

### Actual
```
statusCode: 200
headers: 
    x-powered-by: Express
    content-type: application/json
    link: <http://api.example.com/gists/42>;rel="self", <http://api.example.com/gists/42/star>;rel="star"
    content-length: 257
    etag: W/"101-idYyWiq1HXxBOdpc9zk8qw"
    date: Tue, 21 Feb 2017 22:08:31 GMT
    connection: close

body: 
{
  "created_at": "2017-02-21T22:08:31.135Z",
  "description": "Gist description...",
  "content": "String content...",
  "id": "42",
  "_links": {
    "self": {
      "href": "/gists/#{id}"
    },
    "star": {
      "href": "/gists/#{id}/star"
    }
  }
}

```

## Pass: DELETE /gists/42
## Fail: PATCH /gists/42
### Message
```
headers: Header 'content-type' has value 'application/json' instead of 'application/hal+json'

```

### Request
```
method: PATCH
uri: /gists/42
headers: 
    Content-Type: application/json
    Accept: application/hal+json
    User-Agent: Dredd/2.2.5 (Darwin 15.4.0; x64)
    Content-Length: 44

body: 
{
  "content": "id deserunt Excepteur iru"
}

```

### Expected
```
headers: 
    Content-Type: application/hal+json

body: 
{
  "created_at": "nostrud proident enim laborum elit",
  "description": "voluptate",
  "content": "qui",
  "id": "adipisicing dolor ullamco tempor voluptate",
  "_links": {
    "self": {
      "href": "anim nulla Lorem tempor cillum",
      "templated": false
    }
  }
}
statusCode: 200
bodySchema: {"type":"object","properties":{"created_at":{"type":"string"},"description":{"type":"string"},"content":{"type":"string"},"id":{"type":"string"},"_links":{"type":"object","properties":{"self":{"type":"object","properties":{"href":{"type":"string"},"templated":{"type":"boolean"}},"required":["href"]},"star":{"type":"object","properties":{"href":{"type":"string"},"templated":{"type":"boolean"}},"required":["href"]}},"required":["self"]}},"required":["created_at","description","content","id","_links"]}

```

### Actual
```
statusCode: 200
headers: 
    x-powered-by: Express
    content-type: application/json
    link: <http://api.example.com/gists/42>;rel="self", <http://api.example.com/gists/42/star>;rel="star"
    content-length: 265
    etag: W/"109-Okq1ud/r0oo5Va8imtiVVg"
    date: Tue, 21 Feb 2017 22:08:31 GMT
    connection: close

body: 
{
  "created_at": "2017-02-21T22:08:31.135Z",
  "description": "Gist description...",
  "content": "id deserunt Excepteur iru",
  "id": "42",
  "_links": {
    "self": {
      "href": "/gists/#{id}"
    },
    "star": {
      "href": "/gists/#{id}/star"
    }
  }
}

```

## Fail: GET /gists
### Message
```
headers: Header 'content-type' has value 'application/json' instead of 'application/hal+json'

```

### Request
```
method: GET
uri: /gists
headers: 
    Content-Type: application/json
    Accept: application/hal+json
    User-Agent: Dredd/2.2.5 (Darwin 15.4.0; x64)

body: 


```

### Expected
```
headers: 
    Content-Type: application/hal+json

body: 
{
  "_links": {
    "self": {
      "href": "reprehenderit",
      "templated": true
    }
  },
  "_embedded": {
    "gists": [
      {
        "created_at": "sed eiusmod cillum eu",
        "description": "officia aliquip veniam exerc",
        "content": "do occaecat commodo eu sit",
        "id": "dolore sed aute ullamco",
        "_links": {
          "self": {
            "href": "quis ea elit eiusmod ut",
            "templated": false
          },
          "star": {
            "href": "ut fugiat aliquip amet",
            "templated": true
          }
        }
      },
      {
        "created_at": "culpa consequat nostrud ad pariatur",
        "description": "voluptate officia in",
        "content": "cillum velit nulla ex",
        "id": "laboris velit mollit",
        "_links": {
          "self": {
            "href": "magna adipisicing velit",
            "templated": true
          }
        }
      }
    ]
  },
  "total": -18175189
}
statusCode: 200
bodySchema: {"type":"object","properties":{"_links":{"type":"object","properties":{"self":{"type":"object","properties":{"href":{"type":"string"},"templated":{"type":"boolean"}},"required":["href"]}},"required":["self"]},"_embedded":{"type":"object","properties":{"gists":{"type":"array","items":{"type":"object","properties":{"created_at":{"type":"string"},"description":{"type":"string"},"content":{"type":"string"},"id":{"type":"string"},"_links":{"type":"object","properties":{"self":{"type":"object","properties":{"href":{"type":"string"},"templated":{"type":"boolean"}},"required":["href"]},"star":{"type":"object","properties":{"href":{"type":"string"},"templated":{"type":"boolean"}},"required":["href"]}},"required":["self"]}},"required":["created_at","description","content","id","_links"]}}}},"total":{"type":"number"}},"required":["_links","_embedded","total"]}

```

### Actual
```
statusCode: 200
headers: 
    x-powered-by: Express
    content-type: application/json
    link: <http://api.example.com/gists>;rel="self"
    content-length: 387
    etag: W/"183-ayqwiOV2x1lBVhy684cghA"
    date: Tue, 21 Feb 2017 22:08:31 GMT
    connection: close

body: 
{
  "_links": {
    "self": {
      "href": "/gists"
    }
  },
  "_embedded": {
    "gists": [
      {
        "created_at": "2017-02-21T22:08:31.135Z",
        "description": "Gist description...",
        "content": "String content...",
        "id": "42",
        "_links": {
          "self": {
            "href": "/gists/42"
          }
        }
      }
    ]
  },
  "total": 1
}

```

## Fail: POST /gists
### Message
```
headers: Header 'content-type' has value 'application/json' instead of 'application/hal+json'

```

### Request
```
method: POST
uri: /gists
headers: 
    Content-Type: application/json
    Accept: application/hal+json
    User-Agent: Dredd/2.2.5 (Darwin 15.4.0; x64)
    Content-Length: 67

body: 
{
  "description": "in sunt dolore nostrud in",
  "content": "ad"
}

```

### Expected
```
headers: 
    Content-Type: application/hal+json

body: 
{
  "created_at": "f",
  "description": "in ea occaecat fugiat ex",
  "content": "elit velit dolore",
  "id": "ut aute",
  "_links": {
    "self": {
      "href": "cupidatat",
      "templated": true
    }
  }
}
statusCode: 201
bodySchema: {"type":"object","properties":{"created_at":{"type":"string"},"description":{"type":"string"},"content":{"type":"string"},"id":{"type":"string"},"_links":{"type":"object","properties":{"self":{"type":"object","properties":{"href":{"type":"string"},"templated":{"type":"boolean"}},"required":["href"]},"star":{"type":"object","properties":{"href":{"type":"string"},"templated":{"type":"boolean"}},"required":["href"]}},"required":["self"]}},"required":["created_at","description","content","id","_links"]}

```

### Actual
```
statusCode: 201
headers: 
    x-powered-by: Express
    content-type: application/json
    link: <http://api.example.com/gists/58acba5f3bc71c33067f6d35>;rel="self", <http://api.example.com/gists/58acba5f3bc71c33067f6d35/star>;rel="star"
    content-length: 308
    etag: W/"134-qXUQIN6VXGAHxbVEPOn7gA"
    date: Tue, 21 Feb 2017 22:08:31 GMT
    connection: close

body: 
{
  "description": "in sunt dolore nostrud in",
  "content": "ad",
  "created_at": "2017-02-21T22:08:31.362Z",
  "id": "58acba5f3bc71c33067f6d35",
  "_links": {
    "self": {
      "href": "/gists/58acba5f3bc71c33067f6d35"
    },
    "star": {
      "href": "/gists/58acba5f3bc71c33067f6d35/star"
    }
  }
}

```

## Fail: GET /gists/42/star
### Message
```
headers: Header 'content-type' has value 'application/json' instead of 'application/hal+json'

```

### Request
```
method: GET
uri: /gists/42/star
headers: 
    Content-Type: application/json
    Accept: application/hal+json
    User-Agent: Dredd/2.2.5 (Darwin 15.4.0; x64)

body: 


```

### Expected
```
headers: 
    Content-Type: application/hal+json

body: 
{
  "gist_id": "magna aliqua aute qui sed",
  "starred": false,
  "_links": {
    "self": {
      "href": "cupidatat dolor"
    }
  }
}
statusCode: 200
bodySchema: {"type":"object","properties":{"gist_id":{"type":"string"},"starred":{"type":"boolean"},"_links":{"type":"object","properties":{"self":{"type":"object","properties":{"href":{"type":"string"},"templated":{"type":"boolean"}},"required":["href"]}},"required":["self"]}},"required":["gist_id","starred","_links"]}

```

### Actual
```
statusCode: 200
headers: 
    x-powered-by: Express
    content-type: application/json
    link: <http://api.example.com/gists/#{id}/star>;rel="self"
    content-length: 117
    etag: W/"75-8iQCBbo0COlgdhGD5no9AQ"
    date: Tue, 21 Feb 2017 22:08:31 GMT
    connection: close

body: 
{
  "gist_id": "42",
  "starred": true,
  "_links": {
    "self": {
      "href": "/gists/undefined/star"
    }
  }
}

```

## Pass: PUT /gists/42/star
## Pass: DELETE /gists/42/star
