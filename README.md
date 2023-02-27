# Github-action-test
This is a GitHub Actions workflow example to demonstrate building and testing a simple static site using docker-compose.

## Github Actions Workflow
docker-image.yml
```
name: Docker Image CI

on:
  push:
    branches: [ "master" ]
  pull_request:
    branches: [ "master" ]

jobs:

  build:

    runs-on: self-hosted

    steps:
    - uses: actions/checkout@v3
    - name: Build the Docker compose file
      run: docker-compose up -d
```
