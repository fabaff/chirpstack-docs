---
description: Instruction on how to setup the ChirpStack Network Server requirements.
---

# Requirements

The mentioned Debian / Ubuntu instructions have been tested on:

* Ubuntu 18.04 (LTS)
* Debian 10 (Stretch)

## MQTT broker

ChirpStack Network Server makes use of MQTT for publishing and receiving application
payloads. [Mosquitto](http://mosquitto.org/) is a popular open-source MQTT
server, but any MQTT broker implementing MQTT 3.1.1 should work.
In case you install Mosquitto, make sure you install a **recent** version.

### Install

#### Debian / Ubuntu

In order to install Mosquitto, execute the following command:

```bash
sudo apt install mosquitto
```

#### Other platforms

Please refer to the [Mosquitto download](https://mosquitto.org/download/) page
for information about how to setup Mosquitto for your platform.

## PostgreSQL database

ChirpStack Network Server persists the gateway data into a
[PostgreSQL](https://www.postgresql.org) database. Note that PostgreSQL 9.5+
is required.

### Install

#### Debian / Ubuntu

To install PostgreSQL:

```bash
sudo apt install postgresql
```

#### Other platforms

Please refer to the [PostgreSQL download](https://www.postgresql.org/download/)
page for information how to setup PostgreSQL on your platform.

## Redis database

ChirpStack Network Server uses [Redis](http://redis.io) for storing
device-session data and non-persistent data like distributed locks,
deduplication sets and meta-data. 

Notes:
* At least Redis 2.6.0 is required.
* Flushing the Redis database means all devices have to rejoin (OTAA) the network.

### Install

#### Debian / Ubuntu

To Install Redis:

```bash
sudo apt install redis-server
```

#### Other platforms

Please refer to the [Redis](https://redis.io/) documentation for information
about how to setup Redis for your platform.
