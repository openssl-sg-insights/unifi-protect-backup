# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.7.4] - 2022-08-21
No functional changes in this version. This is just to trigger the release CI.
### Added
- Arm docker container
- rclone debugging instructions when using docker

### Fixed
- Documentation error in rclone config path of docker container.

## [0.7.3] - 2022-07-31
### Fixed
- Updated to the 4.0.0 version of pyunifiprotect
- Added rust to the container, and bumped it to alpine 3.16

## [0.7.2] - 2022-07-17
### Fixed
- Updated to the latest version of pyunifiprotect to fix issues introduced in unifi protect 2.1.1

## [0.7.1] - 2022-06-08
### Fixed
- Updated to the latest version of pyunifiprotect to fix issues introduced in unifi protect 2.0.1
- Updated documentation to include how to set up local user accounts on unifi protect

## [0.7.0] - 2022-03-26
### Added
- Added a the ability to change the way the clip files are structured via a template string.
### Fixed
- Fixed issue where event types without clips would attempt (and fail1) to download clips
- Drastically reduced the size of the docker container
- Fixed typos in the documentation
- Some dev dependencies are now not installed as default

## [0.6.0] - 2022-03-18
### Added
- Support for doorbell ring events
- `detection_types` parameter to limit which kinds of events are backed up
### Fixed
- Actually fixed timestamps this time.

## [0.5.3] - 2022-03-11
### Fixed
- Timestamps in filenames and logging now show time in the timezone of the NVR not UTC

## [0.5.2] - 2022-03-10
### Fixed
- rclone delete command now works as expected on windows when spaces are in the file path
- Dockerfile now allows setting of user and group to run as, as well as a default config

## [0.5.1] - 2022-03-07
### Fixed
- rclone command now works as expected on windows when spaces are in the file path

## [0.5.0] - 2022-03-06
### Added
- If `ffprobe` is available, the downloaded clips length is checked and logged
### Fixed
- A time delay has been added before downloading clips to try to resolve an issue where
  downloaded clips were too short

## [0.4.0] - 2022-03-05
### Added
- A `--version` command line option to show the tools version
### Fixed
- Websocket checks are no longer logged in verbosity level 1 to reduce log spam

## [0.3.1] - 2022-02-24
### Fixed
- Now checks if the websocket connection is alive, and attempts to reconnect if it isn't.

## [0.3.0] - 2022-02-22
### Added
- New CLI argument for passing CLI arguments directly to `rclone`.

### Fixed
- A new camera getting added while running no longer crashes the application.
- A timeout during download now correctly retries the download instead of
  abandoning the event.

## [0.2.1] - 2022-02-21
### Fixed
- Retry logging formatting

## [0.2.0] - 2022-02-21
### Added
- Ability to ignore cameras
- Retry failed download/uploads
- More logging
- CI to build `dev` container
- More documentation

### Fixed
- Upload exceptions getting passed silently
- Camera ID -> Name map is no longer only looked up once at the start

## [0.1.1] - 2022-02-20
### Added
- Docker container
- Dependabot
### Changed
- Better project description
### Fixed
- Typos in docs

## [0.1.0] - 2022-02-19
### Added
- First release
