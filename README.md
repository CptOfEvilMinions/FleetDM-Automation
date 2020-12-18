# FleetDM automation with Ansible and Docker

## Generate OpenSSL keys
This project contains with a self-signed OpenSSL ceretificate which should ONLY BE used for testing. Below are instructions to make your own
1. `openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout conf/tls/<name>.key -out conf/tls/<name>.crt`

## Set Fleet JWT key
This project has a pre-defined JWT key of `super_secret_key_here` which should ONLY BE used for testing. Below are instructions to make your own
1. `openssl rand -base64 32`
1. Copy key and paste in `conf/fleet/fleet.yml` as the value for `jwt_key`

## Docker v2.2
1. `docker-compose build`
1. `docker-compose run --rm fleet fleet prepare db --config /etc/fleet/fleet.yml`
    1. Initializes Kolid database
1. `docker-compose up -d`

## Docker Swarm v3.3
1. `docker stack deploy -c docker-compose-stack.yml fleetdm`
1. `docker service logs -f fleetdm_fleet`

## Ansible

## Versions supported
* `Fleet FleetDM v3.5.1`
* `Ansible v2.11+`
* `Ubuntu server 20.04`

## References
* [How to do a Docker healthcheck with wget instead of curl?](https://stackoverflow.com/questions/47722898/how-to-do-a-docker-healthcheck-with-wget-instead-of-curl)
* [NGINX - Enabling Session Persistence](https://docs.nginx.com/nginx/admin-guide/load-balancer/http-load-balancer/#enabling-session-persistence)
* [Docker - restart policy](https://docs.docker.com/compose/compose-file/#restart_policy)
* [fleetdm/osquery-in-a-box](https://github.com/fleetdm/osquery-in-a-box/blob/master/docker-compose.yml)
* [docker service logs](https://docs.docker.com/engine/reference/commandline/service_logs/)
* [Use Docker Secrets With MySQL on Docker Swarm](https://blog.ruanbekker.com/blog/2017/11/23/use-docker-secrets-with-mysql-on-docker-swarm/)
* [Configuring The Fleet Binary](https://github.com/fleetdm/fleet/blob/master/docs/infrastructure/configuring-the-fleet-binary.md)
* []()
* []()
* []()
* []()
* []()
* []()
* []()
* []()