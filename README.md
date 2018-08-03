# fluentd-s3

[![Build Status](https://travis-ci.org/GovTechSG/fluentd-s3.svg?branch=master)](https://travis-ci.org/GovTechSG/fluentd-s3)

This repository is an automated build job for a docker image containing fluentd service with a s3 plugin installed and ready to use as an *output_plugin*.

S3 Plugin is typically used to watch and tail some log files and output it to s3, a useful scenario to use this is a sidecar to a kubernetes container, mounting the log volume to both containers and this fluentd container will send the logs to S3 possibly as a backup storage, or for AWS Athena query to be ran on.

## Plugins Available

- fluent-plugin-s3 [fluent/fluent-plugin-s3](https://github.com/fluent/fluent-plugin-s3)

## Descriptions

### `latest`

Basically [fluentd-plugin-s3](#fluent-plugin-s3)

### `fluent-plugin-s3`

Canonical Tag: `fluentd-<FLUENTD-VERSION>_fluent-plugin-s3-<PLUGIN_VERSION>`

Latest URL: `fluentd-<FLUENTD-VERSION>_fluent-plugin-s3-latest`

## Usage

#### Running
> docker run -v ${PWD}/fluent.conf:/fluentd/etc/fluent.conf -it govtechsg/fluentd-s3:latest


#### Available commands in container

Outputs fluentd and plugin versions

> version-info

## License

Available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).
