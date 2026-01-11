## Infrastructure

## Bare Metal

#### Pretty Colors LED

**Optional**: apt-get openrgb

```bash
openrgb -d 1 -c B7D455 -d 0 -c B7D455 -d 2 -m Breathing -c a0c17f -s 1
```
see [[Hardware Specs]]

IP : 10.0.0.72
PORT: 8006
### Head Node (VM ID: 100)

- **IP Address:**  10.0.0.110
- **User:** head
- **OS:** Ubuntu Server 24.04.3
- **Resources:**
    - 2 CPU cores
    - 5 GB RAM
    - 50 GB storage

### Worker Node 1 (VM ID: 200) #Apps

- **IP Address:** 10.0.0.234
- **User:** worker-1
- **OS:** Ubuntu Server 24.04.3
- **Resources:**
    - 3 CPU cores
    - 8 GB RAM
    - 32 GB storage

### Worker Node 2 (VM ID: 200) #AI
- IP Address: 10.0.0.224
- User: worker-2
- OS: Ubuntu Server 24.04.3
- Resources:
	- 6 CPU cores
	- 16 GB RAM
	- 60 GB storage space
	- GPU passthrough
---
## Setup Steps

### 1. Initialize Head Node (Server)

SSH into the head node and run:

bash

```bash
# Install K3S server
curl -sfL https://get.k3s.io | sh -

# Verify installation
sudo k3s kubectl get node

# Start K3S server (if not already running)
sudo systemctl start k3s

# Check status
sudo systemctl status k3s
```

### 2. Get Server Token

On the head node:

bash

```bash
sudo cat /var/lib/rancher/k3s/server/node-token
```

Save this token - you'll need it for worker nodes.

### 3. Join Worker Nodes

On each worker node, run:

bash

```bash
curl -sfL https://get.k3s.io | \
  K3S_URL= <ip-address-of-head-node>:6443 \
  K3S_TOKEN=<your-token-here> \
  sh -
```

### 4. Verify Cluster

Back on the head node:

bash

```bash
sudo k3s kubectl get nodes
```