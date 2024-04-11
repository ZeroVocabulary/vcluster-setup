# vcluster-setup
Setup vclusters from an existing cluster, and make a kubeconfig file for access. The Kubernetes api will be accessible via nodeport, which means the node IP must be a static/reserved IP (otherwise it may randomly change and invalidate the config).

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
https://www.vcluster.com/docs/using-vclusters/access#via-nodeport-service

The link does not tell you how to use the port; you have to add it to the kubeconfig after retrieving it.