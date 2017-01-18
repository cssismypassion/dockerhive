# dockerhive
🐝 dockerhive is a collection of helpful scripts to kickstart and support a Docker-based dev environment.

## Prerequisites
Docker `~1.12.6`

dockerhive scripts are shell scripts which run with a shebang line of `#!/usr/bin/env bash`. macOS and Linux-based operating systems should be compatible with this by default.

## Setup
1. Copy the `bin/` folder into your project directory, as well as `Dockerfile` and `docker-compose.yml`.
2. Modify the following files to match your project needs:
  * `Dockerfile`: Choose a base image from the Docker hub.
  * `docker-compose.yml`: Add settings for your Docker container.
  * `bin/dockerhive`: By default the initialization task at the bottom of the file assumes your Docker container is named "web".
  * `bin/run`: By default the run command assumes your Docker container is named "web".
  * `bin/help`: Add a help line for any custom tasks you would like to include.
3. Run `bin/dockerhive` to test that it's all working correctly.

## Usage

When setup is complete and pushed to your version control system, you or your team can pull and run `bin/dockerhive`. If configured correctly, this will be the only step needed for the Docker environment to be built, launched, and initialized in the background. One-off commands can be run against it by using `docker-compose exec`.

## Coming Soon

- Yeoman (or similar) generator for interactive setup, preventing the need to edit the files as described in the Setup section.
- Default quick-start for fresh projects based on pre-supplied Docker configurations.
