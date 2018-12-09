---
title: Mothership REST API
language_tabs:
  - shell: Shell
  - http: HTTP
  - javascript: JavaScript
  - javascript--nodejs: Node.JS
  - ruby: Ruby
  - python: Python
  - java: Java
  - go: Go
toc_footers: []
includes: []
search: true
highlight_theme: darkula
headingLevel: 2

---

<h1 id="mothership">Mothership v1.0.0</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

The official, public REST API for Mothership.

Base URLs:

* <a href="https://app.mothership.cloud/api">https://app.mothership.cloud/api</a>

# Authentication

- oAuth2 authentication.

<h1 id="mothership-app">app</h1>

An application is a logical container for relating specific configuration environments together.

## app.getApps

<a id="opIdapp.getApps"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/apps \
  -H 'Accept: application/json'

```

```http
GET /api/apps HTTP/1.1

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '/api/apps',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const fetch = require('node-fetch');

const headers = {
  'Accept':'application/json'

};

fetch('/api/apps',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/apps',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/apps', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("/api/apps");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},

    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/apps", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /apps`

> Example responses

> 200 Response

```json
[
  {
    "name": "string",
    "slug": "string",
    "description": "string",
    "account": "string",
    "active": false,
    "createdAt": "2018-12-09T04:42:21Z",
    "createdBy": "string",
    "modifiedAt": "2018-12-09T04:42:21Z",
    "modifiedBy": "string",
    "id": "string"
  }
]
```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<name>string</name>
<slug>string</slug>
<description>string</description>
<account>string</account>
<active>false</active>
<createdAt>2018-12-09T04:42:21Z</createdAt>
<createdBy>string</createdBy>
<modifiedAt>2018-12-09T04:42:21Z</modifiedAt>
<modifiedBy>string</modifiedBy>
<id>string</id>
```

<h3 id="app.getapps-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Request was successful|Inline|

<h3 id="app.getapps-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|[[app](#schemaapp)]|false|none|none|
|» name|string|true|none|none|
|» slug|string|false|none|none|
|» description|string|false|none|none|
|» account|string|true|none|none|
|» active|boolean|false|none|none|
|» createdAt|string(date-time)|false|none|none|
|» createdBy|string|false|none|none|
|» modifiedAt|string(date-time)|false|none|none|
|» modifiedBy|string|false|none|none|
|» id|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

## app.createApp

<a id="opIdapp.createApp"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /api/apps \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST /api/apps HTTP/1.1

Content-Type: application/json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: '/api/apps',
  method: 'post',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const fetch = require('node-fetch');
const inputBody = '{
  "name": "string",
  "slug": "string",
  "description": "string",
  "account": "string",
  "active": false,
  "createdAt": "2018-12-09T04:42:21Z",
  "createdBy": "string",
  "modifiedAt": "2018-12-09T04:42:21Z",
  "modifiedBy": "string",
  "id": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('/api/apps',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post '/api/apps',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('/api/apps', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("/api/apps");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},

    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/apps", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /apps`

> Body parameter

```json
{
  "name": "string",
  "slug": "string",
  "description": "string",
  "account": "string",
  "active": false,
  "createdAt": "2018-12-09T04:42:21Z",
  "createdBy": "string",
  "modifiedAt": "2018-12-09T04:42:21Z",
  "modifiedBy": "string",
  "id": "string"
}
```

```yaml
name: string
slug: string
description: string
account: string
active: false
createdAt: '2018-12-09T04:42:21Z'
createdBy: string
modifiedAt: '2018-12-09T04:42:21Z'
modifiedBy: string
id: string

```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<app>
  <name>string</name>
  <slug>string</slug>
  <description>string</description>
  <account>string</account>
  <active>false</active>
  <createdAt>2018-12-09T04:42:21Z</createdAt>
  <createdBy>string</createdBy>
  <modifiedAt>2018-12-09T04:42:21Z</modifiedAt>
  <modifiedBy>string</modifiedBy>
  <id>string</id>
</app>
```

<h3 id="app.createapp-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[app](#schemaapp)|true|none|

> Example responses

> 200 Response

```json
{
  "name": "string",
  "slug": "string",
  "description": "string",
  "account": "string",
  "active": false,
  "createdAt": "2018-12-09T04:42:21Z",
  "createdBy": "string",
  "modifiedAt": "2018-12-09T04:42:21Z",
  "modifiedBy": "string",
  "id": "string"
}
```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<app>
  <name>string</name>
  <slug>string</slug>
  <description>string</description>
  <account>string</account>
  <active>false</active>
  <createdAt>2018-12-09T04:42:21Z</createdAt>
  <createdBy>string</createdBy>
  <modifiedAt>2018-12-09T04:42:21Z</modifiedAt>
  <modifiedBy>string</modifiedBy>
  <id>string</id>
</app>
```

<h3 id="app.createapp-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Request was successful|[app](#schemaapp)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

## app.getApp

<a id="opIdapp.getApp"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/apps/{slug} \
  -H 'Accept: application/json'

```

```http
GET /api/apps/{slug} HTTP/1.1

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '/api/apps/{slug}',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const fetch = require('node-fetch');

const headers = {
  'Accept':'application/json'

};

fetch('/api/apps/{slug}',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/apps/{slug}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/apps/{slug}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("/api/apps/{slug}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},

    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/apps/{slug}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /apps/{slug}`

<h3 id="app.getapp-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|slug|path|string|true|none|

> Example responses

> 200 Response

```json
{
  "name": "string",
  "slug": "string",
  "description": "string",
  "account": "string",
  "active": false,
  "createdAt": "2018-12-09T04:42:21Z",
  "createdBy": "string",
  "modifiedAt": "2018-12-09T04:42:21Z",
  "modifiedBy": "string",
  "id": "string"
}
```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<app>
  <name>string</name>
  <slug>string</slug>
  <description>string</description>
  <account>string</account>
  <active>false</active>
  <createdAt>2018-12-09T04:42:21Z</createdAt>
  <createdBy>string</createdBy>
  <modifiedAt>2018-12-09T04:42:21Z</modifiedAt>
  <modifiedBy>string</modifiedBy>
  <id>string</id>
</app>
```

<h3 id="app.getapp-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Request was successful|[app](#schemaapp)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

## app.updateApp

<a id="opIdapp.updateApp"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT /api/apps/{slug} \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
PUT /api/apps/{slug} HTTP/1.1

Content-Type: application/json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: '/api/apps/{slug}',
  method: 'put',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const fetch = require('node-fetch');
const inputBody = '{
  "name": "string",
  "slug": "string",
  "description": "string",
  "account": "string",
  "active": false,
  "createdAt": "2018-12-09T04:42:21Z",
  "createdBy": "string",
  "modifiedAt": "2018-12-09T04:42:21Z",
  "modifiedBy": "string",
  "id": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('/api/apps/{slug}',
{
  method: 'PUT',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.put '/api/apps/{slug}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.put('/api/apps/{slug}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("/api/apps/{slug}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},

    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/apps/{slug}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /apps/{slug}`

> Body parameter

```json
{
  "name": "string",
  "slug": "string",
  "description": "string",
  "account": "string",
  "active": false,
  "createdAt": "2018-12-09T04:42:21Z",
  "createdBy": "string",
  "modifiedAt": "2018-12-09T04:42:21Z",
  "modifiedBy": "string",
  "id": "string"
}
```

```yaml
name: string
slug: string
description: string
account: string
active: false
createdAt: '2018-12-09T04:42:21Z'
createdBy: string
modifiedAt: '2018-12-09T04:42:21Z'
modifiedBy: string
id: string

```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<app>
  <name>string</name>
  <slug>string</slug>
  <description>string</description>
  <account>string</account>
  <active>false</active>
  <createdAt>2018-12-09T04:42:21Z</createdAt>
  <createdBy>string</createdBy>
  <modifiedAt>2018-12-09T04:42:21Z</modifiedAt>
  <modifiedBy>string</modifiedBy>
  <id>string</id>
</app>
```

<h3 id="app.updateapp-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|slug|path|string|true|none|
|body|body|[app](#schemaapp)|false|none|

> Example responses

> 200 Response

```json
{
  "name": "string",
  "slug": "string",
  "description": "string",
  "account": "string",
  "active": false,
  "createdAt": "2018-12-09T04:42:21Z",
  "createdBy": "string",
  "modifiedAt": "2018-12-09T04:42:21Z",
  "modifiedBy": "string",
  "id": "string"
}
```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<app>
  <name>string</name>
  <slug>string</slug>
  <description>string</description>
  <account>string</account>
  <active>false</active>
  <createdAt>2018-12-09T04:42:21Z</createdAt>
  <createdBy>string</createdBy>
  <modifiedAt>2018-12-09T04:42:21Z</modifiedAt>
  <modifiedBy>string</modifiedBy>
  <id>string</id>
</app>
```

<h3 id="app.updateapp-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Request was successful|[app](#schemaapp)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

## app.deleteApp

<a id="opIdapp.deleteApp"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE /api/apps/{slug}

```

```http
DELETE /api/apps/{slug} HTTP/1.1

```

```javascript

$.ajax({
  url: '/api/apps/{slug}',
  method: 'delete',

  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const fetch = require('node-fetch');

fetch('/api/apps/{slug}',
{
  method: 'DELETE'

})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.delete '/api/apps/{slug}',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.delete('/api/apps/{slug}', params={

)

print r.json()

```

```java
URL obj = new URL("/api/apps/{slug}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "/api/apps/{slug}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /apps/{slug}`

<h3 id="app.deleteapp-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|slug|path|string|true|none|

<h3 id="app.deleteapp-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|Request was successful|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

## app.getConfigs

<a id="opIdapp.getConfigs"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/apps/{slug}/configs \
  -H 'Accept: application/json'

```

```http
GET /api/apps/{slug}/configs HTTP/1.1

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '/api/apps/{slug}/configs',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const fetch = require('node-fetch');

const headers = {
  'Accept':'application/json'

};

fetch('/api/apps/{slug}/configs',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/apps/{slug}/configs',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/apps/{slug}/configs', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("/api/apps/{slug}/configs");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},

    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/apps/{slug}/configs", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /apps/{slug}/configs`

<h3 id="app.getconfigs-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|slug|path|string|true|none|

> Example responses

> 200 Response

```json
[
  {
    "app": "string",
    "env": "string",
    "json": {},
    "auth_key": "string",
    "account": "string",
    "status": "draft",
    "createdAt": "2018-12-09T04:42:21Z",
    "createdBy": "string",
    "modifiedAt": "2018-12-09T04:42:21Z",
    "modifiedBy": "string",
    "id": "string"
  }
]
```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<app>string</app>
<env>string</env>
<json/>
<auth_key>string</auth_key>
<account>string</account>
<status>draft</status>
<createdAt>2018-12-09T04:42:21Z</createdAt>
<createdBy>string</createdBy>
<modifiedAt>2018-12-09T04:42:21Z</modifiedAt>
<modifiedBy>string</modifiedBy>
<id>string</id>
```

<h3 id="app.getconfigs-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Request was successful|Inline|

<h3 id="app.getconfigs-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|[[config](#schemaconfig)]|false|none|none|
|» app|string|true|none|none|
|» env|string|true|none|none|
|» json|object|false|none|none|
|» auth_key|string|false|none|none|
|» account|string|true|none|none|
|» status|string|true|none|none|
|» createdAt|string(date-time)|false|none|none|
|» createdBy|string|false|none|none|
|» modifiedAt|string(date-time)|false|none|none|
|» modifiedBy|string|false|none|none|
|» id|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

## app.createConfig

<a id="opIdapp.createConfig"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /api/apps/{slug}/configs \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST /api/apps/{slug}/configs HTTP/1.1

Content-Type: application/json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: '/api/apps/{slug}/configs',
  method: 'post',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const fetch = require('node-fetch');
const inputBody = '{}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('/api/apps/{slug}/configs',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post '/api/apps/{slug}/configs',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('/api/apps/{slug}/configs', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("/api/apps/{slug}/configs");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},

    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/apps/{slug}/configs", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /apps/{slug}/configs`

> Body parameter

```json
{}
```

```yaml
{}

```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
```

<h3 id="app.createconfig-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|slug|path|string|true|none|
|body|body|[app.createConfigConfig](#schemaapp.createconfigconfig)|true|none|

> Example responses

> 200 Response

```json
{
  "app": "string",
  "env": "string",
  "json": {},
  "auth_key": "string",
  "account": "string",
  "status": "draft",
  "createdAt": "2018-12-09T04:42:21Z",
  "createdBy": "string",
  "modifiedAt": "2018-12-09T04:42:21Z",
  "modifiedBy": "string",
  "id": "string"
}
```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<config>
  <app>string</app>
  <env>string</env>
  <json/>
  <auth_key>string</auth_key>
  <account>string</account>
  <status>draft</status>
  <createdAt>2018-12-09T04:42:21Z</createdAt>
  <createdBy>string</createdBy>
  <modifiedAt>2018-12-09T04:42:21Z</modifiedAt>
  <modifiedBy>string</modifiedBy>
  <id>string</id>
</config>
```

<h3 id="app.createconfig-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Request was successful|[config](#schemaconfig)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

## app.getConfig

<a id="opIdapp.getConfig"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/apps/{slug}/configs/{env} \
  -H 'Accept: application/json'

```

```http
GET /api/apps/{slug}/configs/{env} HTTP/1.1

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '/api/apps/{slug}/configs/{env}',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const fetch = require('node-fetch');

const headers = {
  'Accept':'application/json'

};

fetch('/api/apps/{slug}/configs/{env}',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/apps/{slug}/configs/{env}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/apps/{slug}/configs/{env}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("/api/apps/{slug}/configs/{env}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},

    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/apps/{slug}/configs/{env}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /apps/{slug}/configs/{env}`

<h3 id="app.getconfig-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|slug|path|string|true|none|
|env|path|string|true|none|
|compiled|query|boolean|false|none|

> Example responses

> 200 Response

```json
{
  "app": "string",
  "env": "string",
  "json": {},
  "auth_key": "string",
  "account": "string",
  "status": "draft",
  "createdAt": "2018-12-09T04:42:21Z",
  "createdBy": "string",
  "modifiedAt": "2018-12-09T04:42:21Z",
  "modifiedBy": "string",
  "id": "string"
}
```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<config>
  <app>string</app>
  <env>string</env>
  <json/>
  <auth_key>string</auth_key>
  <account>string</account>
  <status>draft</status>
  <createdAt>2018-12-09T04:42:21Z</createdAt>
  <createdBy>string</createdBy>
  <modifiedAt>2018-12-09T04:42:21Z</modifiedAt>
  <modifiedBy>string</modifiedBy>
  <id>string</id>
</config>
```

<h3 id="app.getconfig-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Request was successful|[config](#schemaconfig)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

## app.updateConfig

<a id="opIdapp.updateConfig"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT /api/apps/{slug}/configs/{env} \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
PUT /api/apps/{slug}/configs/{env} HTTP/1.1

Content-Type: application/json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: '/api/apps/{slug}/configs/{env}',
  method: 'put',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const fetch = require('node-fetch');
const inputBody = '{}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('/api/apps/{slug}/configs/{env}',
{
  method: 'PUT',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.put '/api/apps/{slug}/configs/{env}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.put('/api/apps/{slug}/configs/{env}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("/api/apps/{slug}/configs/{env}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},

    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/apps/{slug}/configs/{env}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /apps/{slug}/configs/{env}`

> Body parameter

```json
{}
```

```yaml
{}

```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
```

<h3 id="app.updateconfig-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|slug|path|string|true|none|
|env|path|string|true|none|
|body|body|[app.createConfigConfig](#schemaapp.createconfigconfig)|true|none|

> Example responses

> 200 Response

```json
{
  "app": "string",
  "env": "string",
  "json": {},
  "auth_key": "string",
  "account": "string",
  "status": "draft",
  "createdAt": "2018-12-09T04:42:21Z",
  "createdBy": "string",
  "modifiedAt": "2018-12-09T04:42:21Z",
  "modifiedBy": "string",
  "id": "string"
}
```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<config>
  <app>string</app>
  <env>string</env>
  <json/>
  <auth_key>string</auth_key>
  <account>string</account>
  <status>draft</status>
  <createdAt>2018-12-09T04:42:21Z</createdAt>
  <createdBy>string</createdBy>
  <modifiedAt>2018-12-09T04:42:21Z</modifiedAt>
  <modifiedBy>string</modifiedBy>
  <id>string</id>
</config>
```

<h3 id="app.updateconfig-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Request was successful|[config](#schemaconfig)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

## app.deleteConfig

<a id="opIdapp.deleteConfig"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE /api/apps/{slug}/configs/{env}

```

```http
DELETE /api/apps/{slug}/configs/{env} HTTP/1.1

```

```javascript

$.ajax({
  url: '/api/apps/{slug}/configs/{env}',
  method: 'delete',

  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const fetch = require('node-fetch');

fetch('/api/apps/{slug}/configs/{env}',
{
  method: 'DELETE'

})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.delete '/api/apps/{slug}/configs/{env}',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.delete('/api/apps/{slug}/configs/{env}', params={

)

print r.json()

```

```java
URL obj = new URL("/api/apps/{slug}/configs/{env}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "/api/apps/{slug}/configs/{env}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /apps/{slug}/configs/{env}`

<h3 id="app.deleteconfig-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|slug|path|string|true|none|
|env|path|string|true|none|

<h3 id="app.deleteconfig-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|Request was successful|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

## app.getKeys

<a id="opIdapp.getKeys"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/apps/{slug}/keys \
  -H 'Accept: application/json'

```

```http
GET /api/apps/{slug}/keys HTTP/1.1

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '/api/apps/{slug}/keys',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const fetch = require('node-fetch');

const headers = {
  'Accept':'application/json'

};

fetch('/api/apps/{slug}/keys',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/apps/{slug}/keys',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/apps/{slug}/keys', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("/api/apps/{slug}/keys");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},

    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/apps/{slug}/keys", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /apps/{slug}/keys`

<h3 id="app.getkeys-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|slug|path|string|true|none|

> Example responses

> 200 Response

```json
[
  {
    "type": "string",
    "key": "string",
    "account": "string",
    "app": "string",
    "env": "string",
    "createdAt": "2018-12-09T04:42:21Z",
    "createdBy": "string",
    "modifiedAt": "2018-12-09T04:42:21Z",
    "modifiedBy": "string",
    "id": "string"
  }
]
```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<type>string</type>
<key>string</key>
<account>string</account>
<app>string</app>
<env>string</env>
<createdAt>2018-12-09T04:42:21Z</createdAt>
<createdBy>string</createdBy>
<modifiedAt>2018-12-09T04:42:21Z</modifiedAt>
<modifiedBy>string</modifiedBy>
<id>string</id>
```

<h3 id="app.getkeys-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Request was successful|Inline|

<h3 id="app.getkeys-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|[[key](#schemakey)]|false|none|none|
|» type|string|true|none|none|
|» key|string|true|none|none|
|» account|string|true|none|none|
|» app|string|false|none|none|
|» env|string|false|none|none|
|» createdAt|string(date-time)|false|none|none|
|» createdBy|string|false|none|none|
|» modifiedAt|string(date-time)|false|none|none|
|» modifiedBy|string|false|none|none|
|» id|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

## app.setKey

<a id="opIdapp.setKey"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT /api/apps/{slug}/keys \
  -H 'Accept: application/json'

```

```http
PUT /api/apps/{slug}/keys HTTP/1.1

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '/api/apps/{slug}/keys',
  method: 'put',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const fetch = require('node-fetch');

const headers = {
  'Accept':'application/json'

};

fetch('/api/apps/{slug}/keys',
{
  method: 'PUT',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.put '/api/apps/{slug}/keys',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.put('/api/apps/{slug}/keys', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("/api/apps/{slug}/keys");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},

    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/apps/{slug}/keys", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /apps/{slug}/keys`

<h3 id="app.setkey-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|slug|path|string|true|none|
|env|query|string|false|none|
|key|query|string|false|none|

> Example responses

> 200 Response

```json
[
  {
    "type": "string",
    "key": "string",
    "account": "string",
    "app": "string",
    "env": "string",
    "createdAt": "2018-12-09T04:42:21Z",
    "createdBy": "string",
    "modifiedAt": "2018-12-09T04:42:21Z",
    "modifiedBy": "string",
    "id": "string"
  }
]
```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<type>string</type>
<key>string</key>
<account>string</account>
<app>string</app>
<env>string</env>
<createdAt>2018-12-09T04:42:21Z</createdAt>
<createdBy>string</createdBy>
<modifiedAt>2018-12-09T04:42:21Z</modifiedAt>
<modifiedBy>string</modifiedBy>
<id>string</id>
```

<h3 id="app.setkey-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Request was successful|Inline|

<h3 id="app.setkey-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|[[key](#schemakey)]|false|none|none|
|» type|string|true|none|none|
|» key|string|true|none|none|
|» account|string|true|none|none|
|» app|string|false|none|none|
|» env|string|false|none|none|
|» createdAt|string(date-time)|false|none|none|
|» createdBy|string|false|none|none|
|» modifiedAt|string(date-time)|false|none|none|
|» modifiedBy|string|false|none|none|
|» id|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

<h1 id="mothership-config">config</h1>

A config represents a single environment's specific key/value pairs. Each config is tied to an app.

## config.retrieveConfigByAuthKey

<a id="opIdconfig.retrieveConfigByAuthKey"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/configs/retrieve \
  -H 'Accept: application/json' \
  -H 'X-Config-Key: string'

```

```http
GET /api/configs/retrieve HTTP/1.1

Accept: application/json
X-Config-Key: string

```

```javascript
var headers = {
  'Accept':'application/json',
  'X-Config-Key':'string'

};

$.ajax({
  url: '/api/configs/retrieve',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const fetch = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'X-Config-Key':'string'

};

fetch('/api/configs/retrieve',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-Config-Key' => 'string'
}

result = RestClient.get '/api/configs/retrieve',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'X-Config-Key': 'string'
}

r = requests.get('/api/configs/retrieve', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("/api/configs/retrieve");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        "X-Config-Key": []string{"string"},

    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/configs/retrieve", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /configs/retrieve`

<h3 id="config.retrieveconfigbyauthkey-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|X-Config-Key|header|string|true|none|

> Example responses

> 200 Response

```json
{}
```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
```

<h3 id="config.retrieveconfigbyauthkey-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Request was successful|Inline|

<h3 id="config.retrieveconfigbyauthkey-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

# Schemas

<h2 id="tocSapp">app</h2>

<a id="schemaapp"></a>

```json
{
  "name": "string",
  "slug": "string",
  "description": "string",
  "account": "string",
  "active": false,
  "createdAt": "2018-12-09T04:42:21Z",
  "createdBy": "string",
  "modifiedAt": "2018-12-09T04:42:21Z",
  "modifiedBy": "string",
  "id": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string|true|none|none|
|slug|string|false|none|none|
|description|string|false|none|none|
|account|string|true|none|none|
|active|boolean|false|none|none|
|createdAt|string(date-time)|false|none|none|
|createdBy|string|false|none|none|
|modifiedAt|string(date-time)|false|none|none|
|modifiedBy|string|false|none|none|
|id|string|false|none|none|

<h2 id="tocSconfig">config</h2>

<a id="schemaconfig"></a>

```json
{
  "app": "string",
  "env": "string",
  "json": {},
  "auth_key": "string",
  "account": "string",
  "status": "draft",
  "createdAt": "2018-12-09T04:42:21Z",
  "createdBy": "string",
  "modifiedAt": "2018-12-09T04:42:21Z",
  "modifiedBy": "string",
  "id": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|app|string|true|none|none|
|env|string|true|none|none|
|json|object|false|none|none|
|auth_key|string|false|none|none|
|account|string|true|none|none|
|status|string|true|none|none|
|createdAt|string(date-time)|false|none|none|
|createdBy|string|false|none|none|
|modifiedAt|string(date-time)|false|none|none|
|modifiedBy|string|false|none|none|
|id|string|false|none|none|

<h2 id="tocSkey">key</h2>

<a id="schemakey"></a>

```json
{
  "type": "string",
  "key": "string",
  "account": "string",
  "app": "string",
  "env": "string",
  "createdAt": "2018-12-09T04:42:21Z",
  "createdBy": "string",
  "modifiedAt": "2018-12-09T04:42:21Z",
  "modifiedBy": "string",
  "id": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|type|string|true|none|none|
|key|string|true|none|none|
|account|string|true|none|none|
|app|string|false|none|none|
|env|string|false|none|none|
|createdAt|string(date-time)|false|none|none|
|createdBy|string|false|none|none|
|modifiedAt|string(date-time)|false|none|none|
|modifiedBy|string|false|none|none|
|id|string|false|none|none|