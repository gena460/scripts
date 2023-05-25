# scripts

Extending kubectl

A top-like tool for your Kubernetes cluster.

## Extend kubectl with plugins
This guide demonstrates how to install and write extensions for kubectl. By thinking of core kubectl commands as essential building blocks for interacting with a Kubernetes cluster, a cluster administrator can think of plugins as a means of utilizing these building blocks to create more complex behavior. Plugins extend kubectl with new sub-commands, allowing for new and custom features not included in the main distribution of kubectl.

## Before you begin
You need to have a working kubectl binary installed.


## How to use:

1. Clone repository

2. Go to the folder "scripts"

3. Make executable file "kubeplugin"
  ```
   sudo chmod +x ./kubeplugin
  ```

4. If you want to run from anywhere, place it in your PATH:
  ```
  sudo mv ./kubeplugin /usr/local/bin
  ```

5. Now you can run
  ```
  kubeplugin <resource_type> <namespace>
  ```

## Example:
```
kubeplugin pod kube-system
```
```
Resource: pod, Namespace: kube-system, Name: coredns-59b4f5bbd5-9gpxj, CPU: 1m, Memory: 15Mi
Resource: pod, Namespace: kube-system, Name: local-path-provisioner-76d776f6f9-t72dp, CPU: 1m, Memory: 7Mi
Resource: pod, Namespace: kube-system, Name: metrics-server-7b67f64457-5l6pl, CPU: 3m, Memory: 16Mi
Resource: pod, Namespace: kube-system, Name: svclb-traefik-53c4898f-25k5j, CPU: 0m, Memory: 2Mi
Resource: pod, Namespace: kube-system, Name: traefik-56b8c5fb5c-g5fd9, CPU: 1m, Memory: 29Mi
```