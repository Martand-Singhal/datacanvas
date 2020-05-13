---
title: 'Ship traffic analysis of Marseille port'
subtitle: 'Tracking key metrics for a ship maintenance service provider'
date: 2020-04-30 00:00:00
description: A web app that analyzes the ship traffic at Marseille port in real-time. Built with Python, and Flask for the backend, SQlite for data storage, Vue (javascript) for the front-end, Vega and Vega-lite for graphics, Docker desktop and Docker-compose for packaging the app and Gitlab CI for continuous deployment.
# featured_image: '/images/demo/demo-square.jpg'
---

![](/images/projects/port.jpg)

## Analyze the key metrics to better manage the ship maintenance schedule 

Imagine that you are a ship maintenance service provider for Marseille port. You would like to analyze the traffic at the port. The analysis would help you to effectively handle your resources such as manpower, tooling, material requirements etc. For this, you would like to build a web app so as to track the arrival/departure status, ship length and speed etc. [Here](https://ship-traffic-app.datacanvas.ch) is a demo app that provides these metrics in real-time.

## How is the web app built?

The app scrapes the data of Marseille port in real time from the website Vesselfinder.com. Then it cleans the data and stores it in a SQlite database. The data is served through an API to the frontend application. Web scraping is performed using the Python library Scrapy. Python's Sqlalchemy library is used to interact with the database and the API is created using Flask. The frontend is designed using Vue.js, Html and CSS. The statistical charts are created using Vega and Vega-lite charting libraries. 

The web app is served using Nginx. The relevant components are packaged separately using docker containers and the continuous integration is enabled using Gitlab CI. Finally, the web app is deployed on a Digitalocean droplet. The app code can be found [here](https://gitlab.com/martandsinghal/scrapy-flask-vue-dashboard).