# Fast API (0.1.0) `OAS 3.1`
[More info](https://call.toingg.com/api/openapi.json)


### Servers
<details>
<summary>/api</summary>
<br>
/api
</details>

---

## Default
`POST` /make_toingg/ Make Toingg
Parameters
| Name        | Description |
| ----------- | ----------- |
| apiKey      | string      |
| request body| Schema      |

| responses   | Media type  |
|-----------  | ----------  |
| 200         | Successful Responses|
| 422        |  Validation Error |

### Example:
```sql
{
  "detail": [
    {
      "loc": [
        "string",
        0
      ],
      "msg": "string",
      "type": "string"
    }
  ]
}
```

---

`POST` /make_batch_toingg/ Make Toingg

Parameters
| Name        | Description |
| ----------- | ----------- |
| apiKey      | string      |
| request body| Schema      |

### Example
```sql
{
  "campaign": "string",
  "numberList": {}
}
```

| responses   | Media type  |
|-----------  | ----------  |
| 200         | Successful Responses|
| 422        |  Validation Error |


---

`POST` /send_sms/ Send Sms
Parameters
| Name        | Description |
| ----------- | ----------- |
| apiKey      | string      |
| request body| Schema      |

### Example
```sql
{
  "name": "string",
  "phoneNumber": "string",
  "message": "string"
}
```

---

`POST` /hang_up_call/ Hang Up Call

Parameters
| Name        | Description |
| ----------- | ----------- |
| callSid      | string      |
| apiKey       | string      |

---

`POST` /create_-checkout-session Create Checkout Session
Parameters
- No parameters

Request Body (Schema)
```sql
{
  "apikey": "string"
}
```

---

`POST` /webhook Stripe Webhook
Parameters
- No parameters
- 200 code: Successful Response


---
---

# Schemas
## APIKey
- Apikey: Object string

## HTTPValidationError
- detail : Object array
- Items: loc, msg,type

## ValidationError
- loc : object array < (string | integer)>
  - Items: string #0/ integer #1
- msg : string
- type: string

## makeBatchCallData
- campaign: string
- numberList: object

## makeCallData
- campaign: string
- name: string
- phoneNumber: string

## smsData
- name: string
- phoneNumber: string
- message: string


