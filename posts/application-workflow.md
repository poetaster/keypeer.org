---
title: Application workflow
date: 2023-01-19
permalink: /application-workflow
---

The work flow for the application should remain simple. 

It's still not clear if application IDs, as disctinct from application instance IDs (this users instance of app). will be generated before use of the REST API, or entirely dynamically.


## keypeer registration flow

Formulation from [#4 issue 4](https://github.com/poetaster/keypeer.org/issues/4#issuecomment-1399534932)

1. User clicks on "Subscribe" button
2. Keypeer would generate random API key that user is expected to keep as it's ID and password.
3. Keypeer would use its secret crypto signature and sign API key to create user's TOKEN
4. User would use TOKEN and label his/her payment
5. User would use keypeer API key in the application for requesting services API keys served by keypeer
6. To check payment status, keypeer would again sign received API key and compare with payed tokens

User can use API key to communicate with keypeer and ask for service API keys. User will use token as a tag for the payments.

## registration flow, 2

Formulation originating in [#2 issue 2](https://github.com/poetaster/keypeer.org/issues/2#issuecomment-1404049386) 

1. generate random API key. That's gonna be used as user's secret
2. Use keypeer secret key (only keypeer knows it) to sign the user's API key
3. signature of the API key is user's token
4. User is shown user's API key and token

User can use API key to communicate with keypeer and ask for service API keys. User will use token as a tag for the payments.

## Initial thoughts

This workflow description assumes the former as some form of authentication will probably be part of the workflow.

1. App. first start submit the application instace ID to keypeer (PUT)
2. keypeer aknowledge succeed in storing instance token
3. keypeer immediately check if the token is 'paid' and store state. This could be as simple as checking if the token is listed under contributions at https://opencollective/keypeer 
4. App requests an API key for the application ID (not this instance, but the global key).
5. keypeer sends the api key.
6. Application stores and utilizes key.

That's the simple description of the intention.   
  
