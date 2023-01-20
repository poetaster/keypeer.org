---
title: How does the developer use this thing?
date: 2023-01-19
permalink: /applications
---

The work flow for the application should remain simple. 

It's still not clear if application IDs, as disctinct from application instance IDs (this users instance of app). will be generated before use of the REST API, or entirely dynamically.

This workflow description assumes the former as some form of authentication will probably be part of the workflow.

1. App. first start submit the application instace ID to keypeer (PUT)
2. keypeer aknowledge succeed in stroging instance token
3. keypeer immediately check if the token is 'paid' This could be as simple as checking if the token is listed under contributions at https://opencollective/keypeer 
4. App requests an API key for the application ID (not this instance, but the global key).
5. keypeer sends the api key.
6. Application stores and utilizes key.

That's the simple description of the intention.   
  
