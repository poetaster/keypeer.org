# Abstract: Can you explain the whole project and its expected outcome(s).

The keypeer project provides an API key intermediary service. It will:

  * give communities access to services otherwise requiring proprietary software
  * provide paid services for users of free and open source software (FOSS)
  * provide a service / application agnostic api intermediary
  * minimize the storing and transmission of personal data 
keypeer enables FOSS developers to include a paid third party service in their application and enable it for a user who has donated. Software users are enabled to contribute to the costs of api usage of a variety of apis.

An example. Although the Open Street Maps dataset is freely available, it has to be processed to be served as map tiles and for search/routing. Payment of the services is through application API keys which require the application developer to pay for the service provided to end users. 

The web service keypeer, in REST, will be prototyped in the Python and C++. Client side code will initially be prototyped in javascript and c++. 

We will network with a variety of projects to create a financial commons with transparent financials.  An example intermediary, [Open Collective](https://opencollective.com/europe). 

# Requested amount  50000

# Explain what the requested budget will be used for? 

The budget will cover personal expenses, consulting (legal & security), communication & PR , server hosting, and postage and handling (smiley). 

## Budget

2000 - 4000 :  API access 6 months, for a 'live' test period (assuming mapbox, maptiler, stadia and newsapi.org)
In order to test the system under load, it will require live data.

100 / month x 6  : server hosting, minor expenses

24000 - 6 months developer time (part time, 20 hours a week, 50 Euro/h). 

1-2000 - Consulting with API service providers and payment processors, collectives, etc.

1-2000 - legal consulting. We will no doubt need to do legal risk assesments as also the following.

5-10000 - Independant Audit. A proper final audit of the code could easily cost more.

# Compare your own project with existing or historical efforts.

This is a first, we believe. Which is also why we're doing it since we have no other option.

# What are significant technical challenges you expect to solve during the project, if any?)

The design of the system poses a number of challenges. Some api's can only use single api keys, some can issue ephemeral keys.  This leads rise to a need to support metering of use or dynamic allocation of short lived keys depending on the service provider. 

We anticipate supporting developers of diverse types of software in integrating keypeer will be the most time consuming challenge.

Beside having to support different patterns in application usage, we will also be facing issues with traditional financial models and payment processing. Connecting securely to payment services without sacrificing use anonymity while also being able to do necessary 'accounting' will no doubt be a technical challenge.

Other technical challenges may include homomorphic cryptography of the user / key store. Since multiple high value keys need to be stored, the value store must be entirely encrypted with a scheme like Fast Proxy Re-Encryption for Publish/Subscribe (see: https://eprint.iacr.org/2017/410).

# Describe the ecosystem of the project, and how you will engage with relevant actors and promote the outcomes?

A number of people and projects are already taking part in the discussion. Most important for the purposes of prototyping at this stage are:

https://github.com/rinigus/pure-maps which will be used for testing a number of api's, including maptiler and mapbox, concurrently.

Regarding pure maps: which will be used for testing a number of API's for accessing map data, such as MapTiler and Stadia, concurrently.

As soon as the first stage is ready, we will engage with the other mapping applications (Gnome Maps, uNav, and others). We will promote this new opportunity in relevant mobile and desktop linux and other FOSS communities.

https://github.com/poetaster/allthenews which may be used for testing with the newsapi.org apis.

