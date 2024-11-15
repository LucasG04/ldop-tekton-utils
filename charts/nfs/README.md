Basic chart can be installed with Argo CD in Namespace "nfs".  
Install via helm:
```bash
helm install nfs-server . --namespace nfs -f values.yaml
```

Provisioner has to be installed manually:
```bash
helm install nfs-client-provisioner nfs-subdir-external-provisioner/nfs-subdir-external-provisioner \
  --namespace nfs \
  -f values.yaml
```