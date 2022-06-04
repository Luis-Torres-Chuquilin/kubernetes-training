<!-- @format -->

# Port-Forward in a POD

Port-forward just words with pods. Then we give a local Port and a remote Port

k port-forward <podName> <localPort>:<RemotePortPodPort>
k port-forward blue 8081:8080

We can access to blue throw localhost:8081

The configuration of blue pod:

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: blue
  labels:
    app: blue-green
    colour: blue
spec:
  containers:
    - name: blue
      image: docker.io/mtinside/blue-green:blue
```
