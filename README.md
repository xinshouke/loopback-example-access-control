#Loopback access control example app
The purpose of this example is to demonstrate [access control list](#!ask rand for acl definition link) usage in [LoopBack](http://loopback.io).

##Contents
- [Overview](#overview)
- [Prerequisites](#prerequisites)
- [Example](#example)
  - [Getting started](#1-getting-started)
  - [Conclusion](#7-conclusion)

##Overview
- what? build an api
- why? to demonstrate how acls help us protect resources

##Prerequisites
This guide assumes you have knowledge of:
- [LoopBack Database Connectors](https://github.com/strongloop/loopback-example-database)
- [LoopBack Models](http://docs.strongloop.com/display/LB/Working+with+models)
- [Authentication and Authorization](http://docs.strongloop.com/display/LB/Authentication+and+authorization)

You should also have the following installed:
- [Node.js](http://nodejs.org/)
- [NPM](http://www.npmjs.com/)
- [StrongLoop Controller](http://strongloop.com/get-started/) `npm install -g strongloop`

##Example
###1. Create the application
[Create a new application](http://docs.strongloop.com/display/LB/Create+a+simple+API#CreateasimpleAPI-Createnewapplication) and name it `loopback-example-access-control`.

###2. Create the models
[Create models](http://docs.strongloop.com/display/LB/Create+a+simple+API#CreateasimpleAPI-Createnewapplication) named `bank`, `account`, `transaction`.
>You can leave the properties empty for this example.

###3. Create the model relations
[Create model relations](http://docs.strongloop.com/display/LB/Creating+model+relations) with the following:

source model|relation|target model|relation name
:-:|:-:|:-:|:-:
user|has many|accessToken|accessTokens
user|has many|accessToken|accessTokens
bank|has many|user|users
bank|has many|account|users
account|has many|transaction|transactions

###4.

###7. Conclusion
