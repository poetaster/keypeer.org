# Abstract: Can you explain the whole project and its expected outcome(s).

see posts/introduction.md

# Have you been involved with projects or organisations relevant to this project before? And if so, can you tell us a bit about your contributions?

A number of people involved with the project, including @poetaser and @rinigus (see ecosystem below) have experience on the developer side using subscription based API keys. It is that experience of the limits and costs of working with these third parties that led to the instigation of the project.

# Requested amount 

# Explain what the requested budget will be used for? 

The budget will cover personal expenses, consulting (security), communication & PR , server hosting, and postage. 

## Budget

4000  -  API access 5 months x 1000 (roughly) api usage for a 'live' test period (assuming mapbox, maptiler, stadia and newsapi.org)
In order to test the system under load, it will require live data.

600 - 100 / month x 6  server hosting, minor expenses

30000 - 6 months developer time (part time, 25 hours a week, 50 Euro/h). 

10000 - Independant Audit. A proper final audit of the code could easily cost more.

# Compare your own project with existing or historical efforts.

This is a first, we believe.

# What are significant technical challenges you expect to solve during the project, if any?)

The design of the system poses a number of challenges. Some api's can only use single api keys, some can issue ephemeral keys.  This leads rise to a need to support metering of use or dynamic allocation of short lived keys depending on the service provider. Either scheme has it's own interesting issues. 

The most challenging technical aspect will be probably be homomorphic cryptography of the user / key store. Since multiple high value keys need to be stored, the value store must be entirely encrypted with a scheme like Fast Proxy Re-Encryption for Publish/Subscribe (see: https://eprint.iacr.org/2017/410).

# Describe the ecosystem of the project, and how you will engage with relevant actors and promote the outcomes?

A number of people and projects are already taking part in the discussion. Most important for the purposes of prototyping at this stage are:

https://github.com/rinigus/pure-maps which will be used for testing a number of api's, including maptiler and mapbox, concurrently

https://github.com/poetaster/allthenews which may be used for testing with the newsapi.org apis.

