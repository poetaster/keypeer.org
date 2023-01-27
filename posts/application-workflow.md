---
title: Application workflow
date: 2023-01-19
permalink: /application-workflow
---

The work flow for the application should remain simple. 

There are several workflows considered on keypeer side. Below, find two workflows that are considered and that will be the base for discussion between developers and other parties.

## keypeer registration flow

Formulation from [#4 issue 4](https://github.com/poetaster/keypeer.org/issues/4#issuecomment-1399534932)

1. User clicks on "Subscribe" button
2. Keypeer would generate random API key that user is expected to keep as ID and password.
3. Keypeer would use its secret crypto signature and sign API key to create user's TOKEN
4. User would use TOKEN and label his/her payment
5. User would use keypeer API key in the application for requesting services API keys served by keypeer
6. To check payment status, keypeer would again sign received API key and compare with payed tokens

## Initial thoughts

This workflow description assumes the former as some form of authentication will probably be part of the workflow.

1. App. first start submit the application instace ID to keypeer (PUT)
2. keypeer aknowledge succeed in storing instance token
3. keypeer immediately check if the token is 'paid' and store state. This could be as simple as checking if the token is listed under contributions at https://opencollective/keypeer 
4. App requests an API key for the application ID (not this instance, but the global key).
5. keypeer sends the api key.
6. Application stores and utilizes key.

That's the simple description of the intention.   
  
