# Create User - POST

POST /v1/user

## Description



* [Request Payloads](#request-payloads)
* [Response Payloads](#response-payloads)

|                                       |                                                 |
| ------------------------------------- | ----------------------------------------------- |
| HTTP Method                           | Post                                         |
| API                                   | User                                           |
| Api Version                           | 1.0.0.3                                         |
| Resource Version                      | 1                                               |
| Summary                               | To create user in the platform                                      |
| Base Path                             | /v1/user                                     |
| Resource                              | Create User                                      |
| Endpoint URL                          | https://api-dev.test.com/v1/user              |
| Service Status                        | Unknown                                         |
| Legislative / Regulatory / Compliance |                                             |
| Firewalls Details                     |                                              |
| Security Certificate Details          |                                              |
| Vendor or Partner Considerations      |                                             |

## Request Payloads

### Request Header


N/A
---

### Query Params


N/A
---

### Request Body

#### Payload 



| Parameter | Description | Sample | PII | Sensitive | Unique Identifier | Mandatory | Default | Details |
| :----- | :-----: | :-----: | :-----: | :-----: | :-----: | :-----: | :-----: | :----- |
| User | &#xA;&#xA;User of the platform&#xA; |  -  | No | No | No | No |  -  | Data Type : object<br>  |
| >User Name |  | tuxx | No | No | Yes | No |  -  | Data Type : string<br> Min. length : 4<br> Max. length : No<br> Regex :  - <br>  |
| >First Name |  | Tu | **Yes** | **Yes** | No | No |  -  | Data Type : string<br> Min. length : 1<br> Max. length : No<br> Regex :  - <br>  |
| >Last Name |  | Bui | **Yes** | **Yes** | No | No |  -  | Data Type : string<br> Min. length : 1<br> Max. length : No<br> Regex :  - <br>  |
| >DoB |  | 1/1/1991 | No | **Yes** | No | No |  -  | Data Type : string<br> Min. length :  - <br> Max. length : No<br> Regex :  - <br>  |
| >Email |  | tu@theapipractice.com | No | **Yes** | Yes | No |  -  | Data Type : string<br> Min. length :  - <br> Max. length : No<br> Regex :  - <br>  |



#### Json sample
```
{
  "userName": "tuxx",
  "firstName": "Tu",
  "lastName": "Bui",
  "dob": "1/1/1991",
  "email": "tu@theapipractice.com"
}
```


#### Json Schema
```
{
  "title": "User",
  "description": "<p>User of the platform</p>",
  "type": "object",
  "properties": {
    "userName": {
      "title": "User Name",
      "type": "string",
      "items": [],
      "minLength": 4,
      "maxLength": 20
    },
    "firstName": {
      "title": "First Name",
      "type": "string",
      "items": [],
      "minLength": 1
    },
    "lastName": {
      "title": "Last Name",
      "type": "string",
      "items": [],
      "minLength": 1
    },
    "dob": {
      "title": "DoB",
      "type": "string",
      "items": []
    },
    "email": {
      "title": "Email",
      "type": "string",
      "items": []
    }
  },
  "required": [
    "userName",
    "firstName",
    "lastName",
    "email"
  ],
  "items": []
}
```

---