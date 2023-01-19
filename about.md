# Introduction

The keypeer project is an api key service.

For developers of Free Open Software (FOSS), keypeer enables them to include a paid service (third party service) in their application and enable it for a user who has donated without having an ongoing business relationship and without storing that user's personal data. Enabling FOSS application users to pay for services allows them to support services that respect privacy and require significant resources.

Often developers simply can't fund the use of third party data or services. Keypeer connects them to users who collectively can supply the financial support.

keypeer enables users to support third party service use in FOSS apps and benifit from those services that they might individually not be able to access without sacrificing privacy. Users often lacks simple and transparent ways to support a project financially and to combine this with the use of the software.

keypeer itself does not accept payment but only registers an anonymous user key / token and associates it to a project related third party service (API key). Management of the payments will be done by a not-for-profit.

# Examples and Social Goals

As an example, many map services require significant data processing and data serving expenses. While OpenStreetMaps dataset is freely available, it has to be processed into specific database formats to be served as map tiles, provide search and routing. Multiple providers exist that are focused in providing privacy respecting service, but the mechanism used for payment of the services is through application API keys where requiring the application developer to pay for the service provided to end users. While it is a viable financial model for proprietary applications, FOSS applications lack a mechanism to enable users to directly pay for the service. Keypeer would enable users to contribute a share of the cost of API calls they make.

Using keypeer, a user application token is created. The user enters this when paying, for example https://opencollective.com/europe. This is registered with keypeer and the app can activate the use of the third party service. Payments are managed by an association, in a collective cash register. This association only initiates payments from the collective account to the third party provider. 

It is not about license purchase for the software itself but the bundling of user payments to pay the third party service, which individual developers or small projects cannot afford.

Some examples of transparent financial intermediaries: https://opencollective.com/europe. https://commonsconservancy.org/ https://www.transnationalgiving.eu/


# Technical Implementation

The technical part consists of a web service (REST API), a freely accessible interface that developers can integrate to distribute user tokens anonymously to keypeer. If the token has been registered with keypeer as paid (according to a reciept token), an additional service can be activated.

User App Token → link to purchase with Token → payment → Token registered with keypeer → User App calls keypeer api, use cleared.

The service will be prototyped in the Python language, probably with the framework, Flask and Werkzeug. An alternative is Gogang.
