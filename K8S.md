All nodes come with container engine (**ie. Docker Runtime**)
# Controller Node

### API Sever
**See** [[Kubectl]]
### ETCD
- key-value store used by k8s stores and replicates cluster states
### Scheduler
- decides where to put pods based on node traffic
### Kubelet
- health checks
- container runtime commands (build, run , stopj)
### Controller Manager

- daemon : embeds controllers into the master node