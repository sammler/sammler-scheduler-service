# sammler-scheduler

> Scheduler for sammler.

[![CircleCI](https://circleci.com/gh/sammler/scheduler-service/tree/master.svg?style=svg)](https://circleci.com/gh/sammler/scheduler-service/tree/master)

## Purpose

<!-- Purpose -->

_sammler-scheduler_ publishes messages to RabbitMQ based on scheduled events (jobs).

It is also the responsibility of _sammler-scheduler_ to store the initial state of jobs (using _sammler-jobs-service_).

## Work in progress

Right now, _sammler-scheduler_ just contains a very basic (and more or less hardcoded) solution, to get messages into the system.

## Install

<!-- Install -->

### Prerequisites

* node >=7.0
* yarn

Install yarn globally:

```sh
$ npm install -g yarn
```

### Clone scheduler service

```sh
$ git clone git@github.com:sammler/scheduler-service.git
```

## Configuration

<!-- Configuration -->

The following environment variables need to be defined for running the service:

* `SAMMLER_RABBITMQ_URI`
* `SAMMLER_JOBS_SERVICE_URI`
* `SAMMLER_LOG_SERVICE_URI`

## Build & Run

<!-- Build & Run -->

Run the development environment:

```sh
$ yarn run dc-dev-up

# Just a shortcut for 
# $ docker-compose f=./docker-compose.dev.yml run --build
```

**Hint:** The development environment relies on some basic services defined in [sammler-base](https://github.com/sammler/sammler-base)

## Author

**Stefan Walther**

* [github/stefanwalther](https://github.com/stefanwalther)
* [twitter/waltherstefan](http://twitter.com/waltherstefan)

## License

Released under the MIT license.

***

_This file was generated by [verb-generate-readme](https://github.com/verbose/verb-generate-readme), v0.2.0, on January 05, 2017._