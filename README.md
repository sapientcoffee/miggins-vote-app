Miggins Voting App
==================

Introduction
------------
This is an example voting app to be used as part of a number of demos, at the moment it is fairly simple and not yet been incorporated into full demos. The plan will be to show with solutions like

* Shipped
* Mantl
* Cloud Center
* Metacloud
* Traditional Application
* Mircoservice Application

At the moment it is based around Docker compose and I have been running and testing on Docker for Mac. I have all the files I have been working on here at the moment however I will start to tidy up once I have a working version I am happy with.

Getting started
---------------

Download [Docker for Mac or Windows](https://www.docker.com).

Run in this directory:

    $ docker-compose up

The app will be running at [http://localhost:5000](http://localhost:5000), and the results will be at [http://localhost:5001](http://localhost:5001).

Architecture
-----

![Architecture diagram](architecture.png)

* A Python webapp which lets you vote between two options
* A Redis queue which collects new votes
* A .NET worker which consumes votes and stores them in…
* A Postgres database backed by a Docker volume
* A Node.js webapp which shows the results of the voting in real time

Credit
------
I have to give credit to a number of different sources. Firstly I used as the base of my voting app something that [https://github.com/docker/example-voting-app](Docker created) and adapted a bootstrap theme called [https://github.com/BlackrockDigital/startbootstrap-freelancer](freelancer).