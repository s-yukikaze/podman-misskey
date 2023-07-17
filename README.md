# Podman-Misskey

This repository provides the sample Podman Kubernetes YAML for Misskey Docker image (https://hub.docker.com/r/misskey/misskey).

# Prerequisites

- Podman

# Getting Started

1. Download the Podman Kubernetes YAML from the repository

```sh
curl -LO https://raw.githubusercontent.com/s-yukikaze/podman-misskey/main/podman-misskey.yml
```

2. Open the the Podman Kubernetes YAML and substitute "changeme" with your UNIX username

3. Create mandatory directories

```sh
mkdir -p ~/.local/{misskey,postgres,redis}
mkdir -p ~/.config/{misskey,redis}
```

4. Download the sample Misskey configuration file form the official repository

```sh
curl -L https://raw.githubusercontent.com/misskey-dev/misskey/develop/.config/docker_example.yml -o ~/.config/misskey/default.yml
```

5. Open the sample Misskey configuration file and substitute the hostnames of Redis and PostgreSQL with "127.0.0.1"

6. Play the Podman Kubernetes YAML

``` sh
podman play kube podman-misskey.yml
```

7. Have fun!

# Lisense

Apache License 2.0 (please read LICENSE for details)