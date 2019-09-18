# Create a photo - POST

POST /v2/photo

## Description



* [Request Payloads](#request-payloads)
* [Response Payloads](#response-payloads)

|                                       |                                                 |
| ------------------------------------- | ----------------------------------------------- |
| HTTP Method                           | Post                                         |
| API                                   | Photo                                           |
| Api Version                           | 2.0.0.0                                         |
| Resource Version                      | 1                                               |
| Summary                               | To create a photo                                      |
| Base Path                             | /v2/photo                                     |
| Resource                              | Create a photo                                      |
| Endpoint URL                          | https://api-dev.test.com/v2/photo              |
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
| Photo |  |  -  | No | No | No | No |  -  | Data Type : object<br>  |
| >File Name | &#xA;&#xA;Name of the photo, extension included&#xA; | myhouse.jpg | No | No | No | No |  -  | Data Type : string<br> Min. length :  - <br> Max. length : No<br> Regex :  - <br>  |
| >Date | &#xA;&#xA;Upload date&#xA; | 1/1/2000 | No | No | No | No |  -  | Data Type : string<br> Min. length :  - <br> Max. length : No<br> Regex :  - <br>  |
| >Description | &#xA;&#xA;Optional.&#xA;&#xA;&#xA;Photo description from user&#xA; | photo of my house | No | No | No | No |  -  | Data Type : string<br> Min. length :  - <br> Max. length : No<br> Regex :  - <br>  |



#### Json sample
```
{
  "fileName": "myhouse.jpg",
  "date": "1/1/2000",
  "description": "photo of my house"
}
```


#### Json Schema
```
{
  "$schema": "http://json-schema.org/draft-04/schema#",
  "title": "Photo",
  "type": "object",
  "properties": {
    "fileName": {
      "title": "File Name",
      "description": "<p>Name of the photo, extension included</p>",
      "type": "string",
      "items": []
    },
    "date": {
      "title": "Date",
      "description": "<p>Upload date</p>",
      "type": "string",
      "items": []
    },
    "description": {
      "title": "Description",
      "description": "<p>Optional.</p><p>Photo description from user</p>",
      "type": "string",
      "items": []
    }
  },
  "required": [
    "fileName",
    "date"
  ],
  "items": []
}
```

---