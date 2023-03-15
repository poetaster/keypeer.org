| Term | Definition
|----|----
| `provider_id` | Internal ID for available services
| `token` | Also refereed to as `payment_token`, used to label payment. Token is of JWT type?
| `keypeer_api_key` | Keypeer API key; provided to apps to connect with keypeer
| `service_api_key` | `provider_id` API key.
| `application_id` | `application` ID.
| `consumer_id` | `end user id` .

---

| Node | Description | Method | Response 
|----|----|----|----
|`/keys/api/{version}/provider/{provider_id}`| Provides the `{provider_id}` `{service_api_key}`  | GET |  `{TOKEN}`, `{keypeer_api_key}`, `datetime`
|`/keys/api/{version}/provider/`| Returns a list of providers | GET |  `{TOKEN}`, `{keypeer_api_key}`, `datetime`
|`/keys/api/{version}/consumer/{consumer_id}` | Request user data |  GET |  [ `application_id`, `provider_id`, `expiry`}, {`application_id`,`provider_id`, `expiry`} ]
|`/keys/api/{version}/consumer/{application_id}`| Add user application | PUT |  `succes` 
|`/keys/api/{version}/consumer/{application_id}`| Retrieve {service_api_key} for application | GET | [`provider_id`, `provider_id`]
|`/keys/api/{version}/application/{application_id}` | Obtain list of application providers  | GET | [`provider_id`, `provider_id`]
|`/keys/api/{version}/application/{application_id}/{provider_id}` | Obtain application provider keys | GET | { `provider_id`, `service_id_key`}, {`provider_id`, `service_id_key`}]
|`/admin/api/{version}/provider/{provider_name}`| Create a new api key provider | PUT |  `provider_id`, `datetime`

---

`/keys/api/{version}/provider` GET
```json
{
  "provider_id": "{application_id}",
  "keypeer_api_key": "service_api_key",
  "token": "token",
}

```
`/keys/api/{version}/provider` `Response`
```json
{
  "service_api_key" : "{service_api_key}",
}
```
---

`/keys/api/{version}/consumer` GET
```json
{
  "consumer_id": "{application_id}", ???
  "keypeer_api_key": "{keypeer_api_key}",
  "application_id": "{application_id}",
}
```

`/keys/api/{version}/consumer` `Response`
```json
{
  "token": "{payment_token}",
  "datetime": "DATETIME",
  "keypeer_api_key": "keypeer_api_key",
  "application_id": "application_id",
  "providers": ["provider_id", "provider_id"],
  "payment_status": [ { "application_id, "status" }, {"application_id", "status"} ],
}
```

---

Should this be in the /admin space?

`/keys/api/{version}/consumer/{application_id}` PUT
```json
{
  "consumer_id": "{consumer_id}",
  "keypeer_api_key": "keypeer_api_key",
  "datetime": "DATETIME",
  "application_id": "{application_id}"
}

```

`/keys/api/{version}/consumer` `Response`
```json
{
  "providers": [{"provider_id", "service_api_key"},],
}
```
---
`/keys/api/{version}/application/{application_id}` GET
```json
{
  "keypeer_api_key": "{keypeer_api_key}",
  "application_id": "{application_id}"
}
```

`/keys/api/{version}/application` `Response`
```json
  "providers": ["{provider_id}", "{provider_id}"], 
  "service_api_key": "{service_api_key}",
  "expiry": "DATETIME"
```
---

`/keys/api/{version}/application/{application_id}/{provider_id}` GET
```json
{
  "keypeer_api_key": "{keypeer_api_key}",
  "application_id": "{application_id}",
  "provider_id": "{provider_id}"
}
```
```
`/keys/api/{version}/application/{application_id/{provider_id}` `Response`
```json
  "service_api_key": "{service_api_key}",
  "expiry": "DATETIME"
```
