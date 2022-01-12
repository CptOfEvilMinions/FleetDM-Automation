# FleetDM-Automation Changelog

<a name="fleet-v4.8.0"></a>
## [fleet-v4.8.0](https://github.com/CptOfEvilMinions/ChooseYourSIEMAdventure/releases/tag/v4.8.0)

[Git Commits](https://github.com/CptOfEvilMinions/FleetDM-Automation/compare/v4.7.0...v4.8.0)

### New Features

* Adding `CHANGELOG.md`

### Under the Hood improvements
- Updated [.env](.env#L2) to use NGINX v1.21.5
- Updated [.env](.env#L1) to use Fleet v4.8.0
- Updated [.env](.env#L10) to use Osquery v5.0.1
- Updated [docker-compose-swarm.yml](docker-compose-swarm.yml#L5) to use `nginx:1.21.5-alpine`
- Updated [docker-compose-swarm.yml](docker-compose-swarm.yml#46) to use `fleetdm/fleet:v4.8.0`


### Bug Fixes

- Removed comments from [.env](.env) file based on [Github issue #17](https://github.com/CptOfEvilMinions/FleetDM-Automation/issues/17)

### CI/CD

- Added GHA workflow to test changes to `docker-compose.yml`
- Added GHA workflow to test changes to `docker-compose-swarm.yml`
- Added GHA workflow to test changes to `deploy_fleetdm.yml`

### Documentation

- Updated Fleet supported version to v4.8.0 on [README](README.md)