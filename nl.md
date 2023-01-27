# Abstract: Can you explain the whole project and its expected outcome(s).

The keypeer will establish a bridge linking end-users and complex online services, the bridge that is missing for free and open source software (FOSS). By allowing end-users to pay for services, it will allow to support services based on open data with transparent payment model instead of privacy abusing ones.

In its core, keypeer provides an API key intermediary service. It will:
- give FOSS communities access to services otherwise requiring proprietary software
- provide a service / application agnostic API intermediary
- minimize the storing and transmission of personal data

Keypeer enables FOSS developers to include a paid service in their application and enable it for a paying users. With keypeer, end-users can contribute to the service costs.

An example: although the OpenStreetMap dataset is freely available, it must be processed for visualization or routing. This requires resources that can be payed for by end-users via keypeer. 

The web service, in REST, will be prototyped in the Python and C++ together with the client side code.

We will network with other projects to create a financial commons with transparent financials, such as OpenCollective.

# Requested amount  50000

# Explain what the requested budget will be used for? 

The budget will cover personal expenses, consulting (legal & security), communication & PR , server hosting, and postage and handling (smiley). 

## Budget

 * 2000 - 4000 :  API access 6 months, for a 'live' test period (assuming mapbox, maptiler, stadia and newsapi.org)
 * 100 / month x 6  : server hosting, minor expenses
 * 24000 - 6 months developer time (part time, 20 hours a week, 50 Euro/h). 
 * 1-2000 - Consulting with API service providers and payment processors, collectives, etc.
 * 1-2000 - legal consulting. We will need to do legal risk assessment as also the following.
 * 5-10000 - Independant security Audit. 

# Compare your own project with existing or historical efforts.

This is a first, we believe. Which is also why we're doing it since we have no other option.

# What are significant technical challenges you expect to solve during the project, if any?)

The design of the system poses a number of challenges. Some api's can only use single api keys, some can issue ephemeral keys.  This leads rise to a need to support metering of use or dynamic allocation of short lived keys depending on the service provider. 

We anticipate supporting developers of diverse types of software in integrating keypeer will be the most time consuming challenge.

Beside having to support different patterns in application usage, we will also be facing issues with traditional financial models and payment processing. Connecting securely to payment services without sacrificing user anonymity while also being able to do necessary 'accounting' will no doubt be a technical challenge.

Other technical challenges may include homomorphic cryptography of the user / key store. Since multiple high value keys need to be stored, the value store must be entirely encrypted with a scheme like Fast Proxy Re-Encryption for Publish/Subscribe (see: https://eprint.iacr.org/2017/410).

# Describe the ecosystem of the project, and how you will engage with relevant actors and promote the outcomes?

A number of people and projects are already taking part in the discussion. Most important for the purposes of prototyping at this stage are:

Puremaps: https://github.com/rinigus/pure-maps which will be used for testing a number of api's, including maptiler and mapbox, concurrently. As soon as the first stage is ready, we will engage with the other mapping applications (Gnome Maps, uNav, and others). We will promote this new opportunity in relevant mobile and desktop linux and other FOSS communities.

Time permitting, we may look at use of news related apis in the context of Journalistic research.  https://github.com/poetaster/allthenews might be used for testing with the newsapi.org apis.

