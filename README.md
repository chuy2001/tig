# Docker TIG stack

Based on the telegraf influxdb grafana office images:

* [telegraf](https://registry.hub.docker.com/_/elasticsearch/)
* [influxdb](https://hub.docker.com/_/influxdb/)
* [grafana](https://hub.docker.com/r/monitoringartist/grafana-xxl/~/dockerfile/)


# Requirements

## Setup

# Usage

Start the ELK stack using *docker-compose*:

```bash
$ docker-compose up
```

You can also choose to run it in background (detached mode):

```bash
$ docker-compose up -d
```
By default, the stack exposes the following ports:
* 3000: grafana for users.
* 8083: influxdb for webui
* 8086: influxdb for telegraf interface
 

*WARNING*: If you're using *boot2docker*, you must access it via the *boot2docker* IP address instead of *localhost*.

*WARNING*: If you're using *Docker Toolbox*, you must access it via the *docker-machine* IP address instead of *localhost*.

# Configuration

*NOTE*: Configuration is not dynamically reloaded, you will need to restart the stack after any change in the configuration of a component.

## How can I tune telegraf configuration?

The telegraf default configuration is stored in `telegraf/config/telegraf.conf`.

## How can I tune influxdb configuration?

The influxdb configuration is stored in `influxdb/config/influxdb.conf`.

