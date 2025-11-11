# selahx

Remote Access Tool — Fast and lightweight CLI experience.

## Features
![Asset/selahx.png](Asset/selahx.png)

## Usage

### Server

Start the server on a specific host and port:

```bash
selahx server --key-file key.pem --port 1221 --ssh-host ubuntu@ec2-xx-xx-xx-xx.compute-1.amazonaws.com
```

Options:

* `--key-file` — Path to the SSH private key
* `--port` — Local port for the server
* `--ssh-host` — SSH host (e.g., `ubuntu@ec2-instance`)

---

### Client

Start a client and connect to the server:

```bash
selahx client --username user --port 1221
```

Options:

* `--username` — Username for the client session
* `--port` — Server port to connect to

---

### Transfer files EC2 to Local

Start saving files.

```bash
selahx save --key-file key.pem --user ubuntu --host ec2-xx-xx-xx-xx.compute-1.amazonaws.com --dest ~/Downloads/test
```

Options:

* `--key-file` — Path to the SSH private key
* `--user` — ubuntu is the user in this case `ssh -i "key.pem" ubuntu@ec2-xx-xx-xx-xx.compute-1.amazonaws.com`
* `--host` — starts from @ i.e `ec2-xx-xx-xx-xx.compute-1.amazonaws.com`
* `--dest` — destination
* `~/Downloads/test` — set your path


## Example Workflow

1. Launch the server on your EC2 instance:

```bash
selahx server --key-file key.pem --port 1221 --ssh-host ubuntu@ec2-xx-xx-xx-xx.compute-1.amazonaws.com
```

2. Connect a client from your local machine:

```bash
selahx client --username user --port 1221
```

Once connected, a reverse SSH tunnel is automatically established.


## Requirements

* Python 3.8+
* Dependencies are managed via Poetry (see `pyproject.toml`)