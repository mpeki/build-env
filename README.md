# Build Environment Action

Uses:
* [actions/checkout](https://github.com/actions/checkout)
* [actions/setup-java](https://github.com/actions/setup-java)
* [docker/login-action](https://github.com/docker/login-action)


# Testing with Act

## 1. Install act (one‑liner)
curl -s https://raw.githubusercontent.com/nektos/act/master/install.sh | sudo bash

## 2. Run the specific job in that workflow
`act -j test`

... or with a specific file:

`act -W .github/workflows/local-test.yml -j test`

# Optional flags
act -v                       # verbose output
act -P ubuntu-latest=ghcr.io/catthehacker/ubuntu:act-latest   # custom runner image
act -s DOCKER_USER=myuser -s DOCKER_PASSWORD=secret           # inject secrets
