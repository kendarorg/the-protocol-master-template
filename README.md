## the-protocol-master-template

### Introduction

A template for protocol master docker compose, it contains working setup for

* TPM-Proxy setup with all settings and all plugins ready
* RabbitMQ
* MySQL (with initialization script)
* Mosquitto (with custom configuration)
* Postgres (with initialization script)
* MongoDB (4.4.2 because don't have a CPU with AVX support....)
* Redis

### How to use

* Download the template
* Remove what you do not need
* Add the applications you need to test/verify/etc to the docker compose
* Set the connection string of the monitored services to "main_tpm:port"
* Have fun!

