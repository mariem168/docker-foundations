# Install Docker & Daemon Tour

## Step 1: Install Docker 24.x on Ubuntu

Run the following commands:

```bash
sudo apt update
sudo apt install ca-certificates curl gnupg
sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | \
  sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg

echo \
  "deb [arch=$(dpkg --print-architecture) \
  signed-by=/etc/apt/keyrings/docker.gpg] \
  https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

sudo apt update
sudo apt install docker-ce docker-ce-cli containerd.io

## Verify installation:
docker --version

## Start Docker daemon:
sudo systemctl start docker
sudo systemctl enable docer 
```

## Step 2: Docker Info Output (Ubuntu 24.04)
Server:
 Containers: 2
  Running: 0
  Paused: 0
  Stopped: 2
 Images: 2
 Server Version: 27.5.1
 Storage Driver: overlay2
  Backing Filesystem: extfs
  Supports d_type: true
  Using metacopy: false
  Native Overlay Diff: true
  userxattr: false
 Logging Driver: json-file
 Cgroup Driver: systemd
 Cgroup Version: 2
 Plugins:
  Volume: local
  Network: bridge host ipvlan macvlan null overlay
  Log: awslogs fluentd gcplogs gelf journald json-file local splunk syslog
 Swarm: inactive
 Runtimes: io.containerd.runc.v2 runc
 Default Runtime: runc
 Init Binary: docker-init
 Security Options:
  apparmor
  seccomp
   Profile: builtin
  cgroupns
 Kernel Version: 6.14.0-24-generic
 Operating System: Ubuntu 24.04.2 LTS
 Architecture: x86_64
 CPUs: 2
 Total Memory: 3.777GiB
 Docker Root Dir: /var/lib/docker

## Step 3: Key Annotations
| Section                 | Meaning / Use                                                                |
| ----------------------- | ---------------------------------------------------------------------------- |
| Containers / Images     | Shows number of total, running, and stopped containers plus available images |
| Server Version          | Docker Engine version (27.5.1) with the latest features                      |
| Storage Driver          | `overlay2`: fast, layered filesystem used in container storage               |
| Logging Driver          | Default: `json-file`; stores logs in JSON format locally                     |
| Cgroup Driver / Version | `systemd` and cgroups v2 for secure and consistent resource management       |
| Security Options        | `apparmor`, `seccomp`, and `cgroupns` provide kernel-level isolation         |
| Kernel & OS             | Ubuntu 24.04.2 + Linux 6.14: supports modern Docker features                 |
| Runtimes                | `runc` is the default OCI runtime for launching containers                   |
| Docker Root Dir         | Default storage path: `/var/lib/docker`                                      |

