Basic chart can be installed with Argo CD in Namespace "nfs".  

Provisioner has to be installed manually:
```bash
helm install nfs-client-provisioner nfs-subdir-external-provisioner/nfs-subdir-external-provisioner \
  --namespace nfs \
  -f values.yaml
```