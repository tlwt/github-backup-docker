# github-backup-docker [![Docker Automated build](https://img.shields.io/docker/automated/jrottenberg/ffmpeg.svg)]()

Dockerized version of [python-github-backup](https://github.com/josegonzalez/python-github-backup) without cron-like behavior. Closes after run completion, so notification can be send to platforms like healthchecks.io

## Install and run

```
docker run --rm --log-driver json-file --log-opt max-size=10m --log-opt max-file=5 -v $(PWD)/backup:/srv/var --name github-backup -h github-backup -e GITHUB_USER=<InsertYourGithubUserHere> -e TOKEN=<InsertYourGithubTokenHere> -e MAX_BACKUPS=10 -e TIME_ZONE=Europe/Berlin github-backup-docker:latest
```
