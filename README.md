# selahx_server
[![Python](https://img.shields.io/badge/python-3.8%2B-blue.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
- Remote Access Tool — Fast and lightweight CLI experience.

- Designed for use with the selahx-client package (https://pypi.org/project/selahx-client/), this enables remote access and management of files and have some control over a local machine from another device.

- Run https://pypi.org/project/selahx_server/ on the target machine, and https://pypi.org/project/selahx-client/ on the machine you want to control it from. Follow each package’s guidelines for how to run it.

---

## Features

overview: https://pypi.org/project/selahx-client/

---

## Usage

### Help

```bash
slx --help
````

![features](https://raw.githubusercontent.com/Haabiy/selahx_server/assets/help.png)

---

### Server

Start the server on a specific host and port:

```bash
slx --key-file key.pem --port 1221 --ssh-host ubuntu@ec2-xx-xx-xx-xx.compute-1.amazonaws.com
````

**Options:**

* `--key-file` — Path to the SSH private key
* `--port` — Local port for the server
* `--ssh-host` — SSH host (e.g., `ubuntu@ec2-xx-xxx-xx-xxx.compute-1.amazonaws.com`)

---

## Example Workflow

1. Launch the server on your EC2 instance:

```bash
slx --key-file key.pem --port 1221 --ssh-host ubuntu@ec2-xx-xx-xx-xx.compute-1.amazonaws.com
```

## Requirements

* Python 3.11+
* Dependencies are managed via Poetry (see `pyproject.toml`)

---