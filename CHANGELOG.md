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

### Bug Fixes

- Removed comments from [.env](.env) file based on [Github issue #17](https://github.com/CptOfEvilMinions/FleetDM-Automation/issues/17)

### CI/CD

- Added GHA workflow to test changes to `docker-compose.yml`
- Added GHA workflow to test changes to `deploy_fleetdm.yml`

### Documentation

- Updated Fleet supported version to v4.8.0 on [README](README.md)