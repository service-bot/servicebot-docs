##Roadmap

###Overview
We have big plans for ServiceBot, below are some of them. If you have an idea 
for a new feature or think we should prioritize on something else, you can post 
on our [community](http://community.servicebot.io/) or pop into [gitter](https://gitter.im/service-bot/Lobby).
This list is not comprehensive and only details major items on our list. There
are many many small improvements that will be included with major releases. 
###Immediate goals

####Refactoring
ServiceBot is still a bit rough around the edges under the hood, the architecture
is solid but some of the pieces could be cleaned up.
####Testing coverage
Our current test suite does not cover nearly enough code, we aim to cover all the APIs and start writing 
unit tests for the model layer
####Open Issues
Major bugs and issues that arise will be an immediate concern of the ServiceBot team
###2017 Goals

####Extensibility Improvements
Being able to extend and develop plugins for ServiceBot is one of our top
priorities in 2017 - we hope to be able to give developers a clear guide on 
how to develop and publish plugins for ServiceBot.

####Wordpress Plugin
We want to allow ServiceBot to be used as a backend system that a Wordpress user can connect to using a plugin which pulls ServiceBot services into Wordpress to be consumed by customers.

####Smarter Forms
The Service Designer lets you build a form for a customer to fill out when requesting a service.
We plan on expanding this form design system to allow for more flexibility with features such as price changes based on inputs,
the ability to pull external data to populate form elements, and more input options such as date, file upload, and location.

###Future Goals

####Localization/i18n
Currently ServiceBot is an english language application, we aim to change this by 
adding in support for multiple locales and languages so it will be easy to swap out any language.
 
####Service Workflows
One of our long term goals is to add more automation capabilities to ServiceBot.
One way we plan on doing this is by adding a workflow system to allow users to define the actual steps 
that are taken in order to fulfill a service and have the workflow run when new services are requested by customers.

####Service Actions
We want there to be actions on a service a user can take, for example a hosting service could have an action to shut down a server, 
or a monthly cleaning service could have an additional action (for a price) which can clean something extra like a garage.



