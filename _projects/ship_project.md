---
title: 'Ship traffic analysis of Marseille port'
subtitle: 'Tracking KPIs for a ship maintenance service provider'
date: 2020-04-30 00:00:00
description: A web app that analyzes the ship traffic in real-time. Built with Python, and Flask for the backend, SQlite for data storage, Vue (javascript) for the front-end, Vega and Vega-lite for graphics, Docker desktop and Docker-compose for packaging the app and Gitlab CI for continuous deployment.
# featured_image: '/images/demo/demo-square.jpg'
---

<!-- ![](/images/demo/demo-landscape.jpg) -->

## Analyze the key performance indicators (KPIs) to best organize the ship maintenance schedule 

Imagine that you are a ship maintenance service provider for Marseille port. You want to better understand the traffic at the port to help you organize your resources such as manpower required, tooling needed, material requirements etc. For this, you would like to build an app that would help you track key ship characteristics such as arrival/departure status, ship length and speed etc. [Here](http://207.154.205.68:8007/) is a demo app that tracks these metrics in real-time (If you have problems opening the app, then please ensure that the **http** connections are not blocked. An ssl certificate is missing for the app to work with https).

## How does the app works?

The app scrapes the data of Marseille port in real time from the site Vesselfinder.com. Then it cleans the data and stores it in SQlite database. The data is served through an API to the frontend application. Web scarping is performed using the Python library Scrapy, Python's Sqlalchemy library is used to interact with the database and the api is created using Flask. The frontend is designed using Vue.js, Html and CSS. The statistical charts are created using Vega and Vega-lite charting libraries. 

The web app is served using Nginx. The relevant components are packaged separately using docker containers and the continuous integration is enabled using Gitlab CI. The web app is deployed on a Digitalocean droplet. The app code can be found [here](https://gitlab.com/martandsinghal/scrapy-flask-vue-dashboard).