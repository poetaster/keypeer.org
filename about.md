# Introduction

For developers of Free Open Software (FOSS), keypeer enables them to include a paid third party service in their application and enable it for a user who has donated without having an ongoing business relationship and without storing that user's personal data. Enabling FOSS application users to pay for services allows them to support services that respect privacy and require significant resources.

The keypeer project provides an api key intermediary service. It aims to serve the following goals:

  * give user communities access to services that would otherwise require proprietary software
  * free developers to provide access to paid services
  * provide a service / application agnostic api to act as an intermeidary
  * avoid the storing and transmission of personal data 

A bird's-eye view of the process.

![An overview of the actors and actions involving keypeer](overview.png)

Keypeer enables users to support third party service use in FOSS apps and benifit from those services that they might individually not be able to access without sacrificing privacy. Users often lack simple and transparent ways to support a project financially and to combine this with the use of the software.  Often developers simply can't fund the use of third party data or services. Keypeer connects them to users who collectively can supply the financial support.

Keypeer itself does not accept payment but only registers an anonymous user key / token and associates it to a project related third party service (API key). Management of the payments will be done by a not-for-profit.

# Examples and Social Goals

As an example, many map services require significant data processing and data serving expenses. While OpenStreetMaps dataset is freely available, it has to be processed into specific database formats to be served as map tiles, provide search and routing. Multiple providers exist that are focused in providing privacy respecting service, but the mechanism used for payment of the services is through application API keys which  require the application developer to pay for the service provided to end users. While it is a viable financial model for proprietary applications, FOSS applications lack a mechanism to enable users to directly pay for the service. Keypeer would enable users to contribute a share of the cost of API calls they make.

Other examples of types of services which require keys or proprietary licenses:

  * transportation authorities, which require use of their apps or limit the use of the apis
  * news service providers like Reuters and AP or the aggregator newsapi.org. These charge upward of 450 USD a month. 
  * text-to-speech, speech-to-text services

Some examples of transparent financial intermediaries: [Open Collective](https://opencollective.com/europe). [Commons Conservancy](https://commonsconservancy.org/) [Transnational Giving](https://www.transnationalgiving.eu/)

# Technical Implementation

The technical part consists of a web service (REST API), a freely accessible interface that developers can use for accessing services API keys through keypeer.

Using keypeer, a user application token is created. This token is specific to an application with it's own token and the installation instance of the user. It is a combined hash of a keypeer application ID and a onetime hash made by the application. The user provides this token when paying, for example https://opencollective.com/europe. This payment is registered with keypeer and the app on querying keypeer can obtain confirmation that this token instance has made a contribution and activate the use of the third party service. Payments are managed by an association, in a collective cash register. This association only initiates payments from the collective account to the third party provider. 

User App Token → link to purchase with Token → payment → Token registered with keypeer → User App calls keypeer api, use cleared.

The service will be prototyped in the Python language, probably with the framework, Flask and Werkzeug. 
