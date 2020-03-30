# e2eApp

I build this app to be able to e2e test multiple databases and other backends with and without TLS inside kubernetes clusters.

There have beeen multiple times in my carer when someone comes to me saying that I can't reach the db or some other backend service.
I want to be able to quickly spin up this application and verify towards a backend service annd give myself decent logs and some metrics.

To veirfy the different backend services I will plan to write and read towards them.
For example when it comes to Kafka I will write to one topic and listen to it at the same time using a rest endpoint to perfrom the write to that topic.
I will have one endpoint per backend service for example:

POST /api/kafka

POST /api/mariadb
GET /api/mariadb

All the configrutaion needed to be able to communicate with the different backend services will need to be set as environment variabels or as a config file.

The plan is that all of the services should be able to be tested with TLS since it's a normal issue.

Depending on time and prio I will also automate setup of the different services that I test with TLS to be able to easily test this.

## What it isn't

This is not a application for production! It's only to perfrom a simple e2e test och a backend service.
It will not be written to perfrom benchmark tests.

## Note

I also want to point out that I'm no master go programer, one of the main reasons why I do this project is that i wan't something to work one
where I can try a number of different libaries and improve my programing skills.

If you have any suggestions on how to make this project better I'm more then happy to take feedback.
