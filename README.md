# vcluster

It uses a nodeport to make the api/control plane accessible, which means node ip must be static.
```
vcluster-setup <vcluster name>
```
The kubeconfig file generates in output/kubeconfig.yaml.

Test the kubeconfig file:
```
kubectl --kubeconfig output/kubeconfig.yaml get namespaces
```

## Notes
Source:
https://www.vcluster.com/docs/operator/external-access#nodeport-service

They do not tell you how to use the port; you have to add it to the kubeconfig after generating it.