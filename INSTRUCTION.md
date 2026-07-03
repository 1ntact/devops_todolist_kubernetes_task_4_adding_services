# To test an app by calling a ClusterIP service DNS from a busybox container. Run this command:

```bash
kubectl run busybox --image=busybox -n todoapp -it --rm -- sh
```

# After, when you finish with testing better to clean data. Simply use this command to delete this container:

```bash
kubectl delete pod busybox -n todoapp
```
# To test ToDo application using the service port-forward command. Run this command:

```bash
kubectl port-forward service/todoapp-service 8081:80 -n todoapp
```


> **Note:** To test the application, open a browser and enter the address in the format `http://<NodeIP>:<NodePort>`,
> replacing `<NodeIP>` with the actual IP address of one of the cluster nodes and `<30007>` with the actual port. 
> In our case, the local cluster does not have publicly accessible IP addresses, so you need to use `http://localhost:<NodePort>`.
