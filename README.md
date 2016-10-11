# EPAM Report Portal
[![Join Slack chat!](https://reportporal-slack-auto.herokuapp.com/badge.svg)](https://reportporal-slack-auto.herokuapp.com)
[![stackoverflow](https://img.shields.io/badge/reportportal-stackoverflow-orange.svg?style=flat)](http://stackoverflow.com/questions/tagged/reportportal)
[![GitHub contributors](https://img.shields.io/github/contributors/reportportal/reportportal.svg?maxAge=2592000)](https://github.com/reportportal/reportportal)
[![Docker Pulls](https://img.shields.io/docker/pulls/reportportal/service-gateway.svg?maxAge=2592000)](https://github.com/reportportal/reportportal)
[![License](https://img.shields.io/badge/license-GPLv3-blue.svg)](http://www.gnu.org/licenses/gpl-3.0.html)
[![Build with Love](https://img.shields.io/badge/build%20with-%E2%9D%A4%EF%B8%8F%E2%80%8D-ff69b4.svg)](http://reportportal.io)


Report Portal organized into multiple repositories.

Application Core based on micro-services architecture and includes list of mandatory services.
> IMAGE: 

## Repositories structure

ReportPortal consists of the following services:
- [`service-registry`](https://github.com/reportportal/service-registry) Redis. Used for distributed cache.
- [`service-authorization`](https://github.com/reportportal/service-authorization) Authorization Service. In charge of access tokens distribution
- [`service-gateway`](https://github.com/reportportal/service-gateway) Gateway Service. Main entry point to application. Port used by gateway should be opened and accessible from outside network.
- [`service-api`](https://github.com/reportportal/service-api) API Service. Application Backend
- [`service-ui`](https://github.com/reportportal/service-ui) UI Service. Application Frontend
- [`service-jira`](https://github.com/reportportal/service-jira) JIRA Service. Interaction with JIRA
- [`service-rally`](https://github.com/reportportal/service-rally) Rally Service. Interaction with Rally

Other repositories stored according to next rules
- `service-*` - micro-services which is a part of Application
- `commons-*` - common libraries, models, etc., used by micro-services

Addapters (client side code) related repositories:

- `client-*` - http clients, which process HTTP request sending
- `agent-*` - custom reporters (mostly custom Listeners), which monitor test events and trigger event sending via client-*
- `logger-*` - logger appenders, which helps to collect logs, wire it with test case via agent-* and send to server via client-*


## Installation steps

### Simple set (small project/demo set) with Docker

1. Install [Docker](http://docs-stage.docker.com/engine/installation/) ([Docker Engine](https://docs.docker.com/engine/installation/), [Compose](https://docs.docker.com/compose/install/), [Swarm](https://docs.docker.com/swarm/install-manual/))
2. Deploy [mongoDB](https://docs.mongodb.com/manual/installation/)
3. Download [Example of compose descriptor](https://github.com/reportportal/reportportal/blob/master/docker-compose.yml) to any folder
3. Deploy ReportPortal using `docker-compose` within the same folder with downloaded compose file

  ```
  docker-compose up 
  ```

>Note: Docker Compose is optional. It's possible to run containers using plain `docker run` mechanism and link it to each other

### Customizable deployment and production ready set with Docker

To customize deployment and make it production ready please follow [detailed installation steps](https://github.com/reportportal/reportportal/blob/master/installation.md)

## Contribution

There are many different ways to contribute to Report Portal's development, just find the one that best fits with your skills. Examples of contributions we would love to receive include:

- **Code patches**
- **Documentation improvements**
- **Translations**
- **Bug reports**
- **Patch reviews**
- **UI enhancements**

Big features are also welcome but if you want to see your contributions included in Report Portal codebase we strongly recommend you start by initiating a chat though our Team.

## Documentation

* [User Manual](http://reportportal.io/#documentation)
* [Wiki and Guides](https://github.com/reportportal/reportportal/wiki)


## Community / Support

* [Open Slack chat](https://reportporal-slack-auto.herokuapp.com)
* Report Portal Google Group (comming soon)
* [GitHub Issues](https://github.com/reportportal/reportportal/issues)
* [Stackoverflow Questions](http://stackoverflow.com/questions/tagged/reportportal)

## License

Report Portal is [GNU General Public License v3.0](http://www.gnu.org/licenses/gpl-3.0.html).

[![HitCount](https://hitt.herokuapp.com/reportportal/reportportal.svg)](https://github.com/reportportal/reportportal)
