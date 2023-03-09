This is a basic API implementation scheme based on the notes in the project's page. It would be useful to push it as a file  to allow for further amendments and contributions. 

The idea behind `{version}` is allow for updates to the system without affecting the current implementation. 

There are a few obfuscation techniques to circumvent interception of key data. These are not necessary and will only add computational overhead.

I had the idea of exposing `{provider_id}`'s API through keypeer for certain services. Something to the effect of  `/api/{version}/{provider_id}/{exposed_api}` which would allow for app requests through keypeer to the {provider_id}. If this is to be implemented, I would argue that it should remain within generic API services the likes of News. Although this would add complexity and therefore unnecessarily bloat the project given the required bandwidth and backend capabilities to achieve it. 
  

| Node | Description | Method | Response 
|----|----|----|----
|`/api/{version}/generate`| It should allow for multiple `{provider_id}` in a singular request.| GET |  `{TOKEN}`
| `/api/{version}/submit` | App submission | POST | `{random_id_of_length_256}`
|`/api/{version}/request/{provider_id}` | API key request given status response from `submit` node|  GET |  `{TOKEN ⊕ instance_id}`
| `/api/{version}/status}` | Generic Status Node, KeyPeer should be included in {provider_id} | GET | `BOOLEAN`

---
`/api/{version}/generate` GET
```json
{
  "provider_id": ["news_service_id", "map_service_id"],
  "datetime": "DATETIME",
  "app": "app_name"
  "...": "...",
}
```
`/api/{version}/generate` `Response`
```json
{
  "_id": "SHA256(SHA256(app_name)+salt)",
  "uid" : "random_bits_of_length_XYZ",
  "datetime": "DATETIME",
  "...": "...",
}
```
---
`/api/{version}/submit` POST
```json
{
  "instance_id": "SHA256((_id+random_bits_of_length_XYZ))",
  "...": "...",
}
```
`/api/{version}/submit` `Response`
```json
{
  "token": "TOKEN ⊕ instance_id",
  "datetime": "DATETIME",
  "...": "..."
}
```
---
`/api/{version}/request/{provider_id}` GET
```json
{
  "token": "TOKEN ⊕ instance_id",
  "...": "...",
}
```

`/api/{version}/request/{provider_id}` `Response`
```json

  "api_key": "api_key ⊕ TOKEN",
  "...": "...",

```
---
`/api/{version}/status` GET

```json

  "provider_id": ["news_service_id", "map_service_id"],
  "...": "...",

```
`/api/{version}/status` `Response`

```json

  "status": "BOOLEAN",
  "...": "...",

```
