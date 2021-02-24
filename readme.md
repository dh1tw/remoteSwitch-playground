# remoteSwitch Playground

This repository contains the sources to the [remoteSwitch](github.com/dh1tw/remoteSwitch) playground at [demo.switch.shackbus.org](demo.switch.shackbus.org).

The playground uses [docker-compose](https://docs.docker.com/compose/) to orchestrate 8 remoteSwitch instances.

![screenshot switch demo1](/images/switch-demo1.png)

## Description

### Instances

#### remoteSwitch instances:
All instances use the *dummy_switch* implementation.

- [8x4 Bandswitch](/switch-demo1/config/bandswitch.toml)
- [10m Stackmatch](/switch-demo1/config/sm10m.toml)
- [15m Stackmatch](/switch-demo1/config/sm15m.toml)
- [20m Stackmatch](/switch-demo1/config/sm20m.toml)
- [40m Antenna Switch](/switch-demo1/config/sw40m.toml)
- [80m Antenna Switch](/switch-demo1/config/sw80m.toml)
- [80m 4-Square](/switch-demo1/config/4sq.toml)

#### Other
- remoteSwitch web (aggregator)
- nats-server (communication backend)

## How to execute

It's pretty easy to run you own demo instance locally if you have
[docker](https://www.docker.com/products/docker-desktop) installed on your machine.

Depending on your OS and CPU's architecture you might have to adjust in the [docker-compose.yml](/switch-demo1/docker-compose.yml) the arguments
- arch
- os
- [release](github.com/dh1tw/remoteSwitch/releases)

Then just run
``` bash
$ docker-compose up --build
```
