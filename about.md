---
title: About keypeer.org 
date: 2023-01-18
permalink: /about.html
---

# keypeer.org

## Introduction

The keypeer project is an api key service.

For developers of Free Open Software (FOSS), keypeer enables them to include a paid service (third party service) in their application and enable it for a user who has donated without having an ongoing business relationship and without storing that user's personal data.

Often developers simply can't fund the use of third party data or services. Keypeer connects them to users who collectively can supply the financial support.

keypeer enables users to support third party service use in FOSS apps and benifit from those services that they might individually not be able to access without sacrificing privacy. Users often lacks simple and transparent ways to support a project financially and to combine this with the use of the software.

keypeer itself does not accept payment but only registers an anonymous user key / token and associates it to a project related third party service (API key). Management of the payments will be done by a not-for-profit.

## Examples and Social Goals

As an example, many FOSS map services offer, besides a base like Openstreetmaps, tiles (eg. satellite) from third parties that are paid for after a certain number of users/views. Mapbox, for example. keypeer would be the interface, the service that allows the user to contribute donations and obtain keys for one or more third party services in a mapping app like pure maps.

Using keypeer, a user<->app token is created. The user enters this when paying, for example https://opencollective.com/europe. This is registered with keypeer and the app can activate the use of the third party service. Payments are managed by an association, in a collective cash register. This association only initiates payments from the collective account to the third party provider or Mapbox.

It is not about lisense purchase for the software itself but the bundling of user payments to pay the third party service, which the developer or the project cannot afford.

Example transparent financial intermediaries: https://opencollective.com/europe. https://commonsconservancy.org/ https://www.transnationalgiving.eu/


## Technical Implementation

The technical part consists of a web service (REST API), a freely accessible interface that developers can integrate to distribute user tokens anonymously to keypeer. If the token has been registered with keypeer as paid (according to rotation), an additional service can be activated.

User App Token -> link to purchase with Token -> payment -> Token registered with keypeer -> User App calls keypeer api, use cleared.

The service will be prototyped in the Python language, probably with the framework, Flask and Werkzeug. An alternative is Gogang.