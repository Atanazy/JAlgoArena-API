# JAlgoArena API [![Build Status](https://travis-ci.org/spolnik/JAlgoArena-API.svg?branch=master)](https://travis-ci.org/spolnik/JAlgoArena-API)

JAlgoArena API is API Gateway service for all backend JAlgoArena services. It's created based on Netflix Zuul with usage of Spring Boot and Spring Cloud.

- [Introduction](#introduction)
- [Components](#components)
- [Continuous Delivery](#continuous-delivery)
- [Infrastructure](#infrastructure)
- [Notes](#notes)

## Introduction

- API Gateway is the single point forwarding to destination service. It's using Eureka for identifying url/addresses of the services just based on their names. Additionally - it has configured client load balancer (Netflix Ribbon) - which load balance requests - it's mainly used in JAlgoArena for many Judge Agents - as they are stateless services and considerably slowest part of JAlgoArena infrastructure.

![Component Diagram](https://github.com/spolnik/JAlgoArena-API/raw/master/design/component_diagram.png)

## Components

- [JAlgoArena](https://github.com/spolnik/JAlgoArena)
- [JAlgoArena UI](https://github.com/spolnik/JAlgoArena-UI)

## Continuous Delivery

- initially, developer push his changes to GitHub
- in next stage, GitHub notifies Travis CI about changes
- Travis CI runs whole continuous integration flow, running compilation, tests and generating reports
- application is deployed into Heroku machine

## Infrastructure

- Heroku (PaaS)
- Spring Boot, Spring Cloud
- Netflix Zuul (api gateway), Ribbon (load balancer), Hystrix (circut breaker)
- TravisCI - https://travis-ci.org/spolnik/JAlgoArena-API

## Notes
- [Running locally](https://github.com/spolnik/jalgoarena/wiki)
- [Travis Builds](https://travis-ci.org/spolnik)

![Component Diagram](https://github.com/spolnik/JAlgoArena/raw/master/design/JAlgoArena_Logo.png)
