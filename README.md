# artifact-drone

Can be used to build drone.io/autoscaler binaries using Hashicorp Packer and docker.
Useful when u got no CI/CD in place and starting things from scratch.

Usage:
##### build
```
packer build -var "tag=v0.8.6" drone-build.json
```
Command above will produce two files in current directory - drone-server.v0.8.6 and drone-agent.v0.8.6. 
Those binaries can already be used.
##### pack
```
packer build -var "tag=v0.8.6" drone-server-container.json
packer build -var "tag=v0.8.6" drone-agent-container.json
```
Now we have docker containers with drone binary as entrypoint.

Same applies for autoscaler.
