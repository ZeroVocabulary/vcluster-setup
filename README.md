# vcluster
```
vcluster-setup <vcluster name>
```
It uses a nodeport to make the api/control plane accessible, which means the node ip must be static.

The kubeconfig file generates in output/kubeconfig.yaml.

Test the kubeconfig file:
```
kubectl --kubeconfig output/kubeconfig.yaml get namespaces
```

## Notes
Source:
https://www.vcluster.com/docs/operator/external-access#nodeport-service

They do not tell you how to use the port; you have to add it to the kubeconfig after retrieving it.

