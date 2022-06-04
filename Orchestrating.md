<!-- @format -->

# Deployment - First Class support - For Stateless

Deployments are good for web services that are [stateless], that are horizontal scalable.
May we need many copies of the same pod to manage the users, to manage that load

To manage more copies of the pod, we can copy the file and just we changed the name and we deploy it

Deployment make a copy of the pod.

```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: blue-green
spec:
  replicas: 3
  selector:
    matchLabels:
      app: blue-green
  template:
    metadata:
      labels:
        app: blue-green
    spec:
      containers:
        - name: blue-green
          image: mtinside/blue-green:blue
```

## Add Plugin tree

k krew install tree

To see the deployment tree

k tree deployment <deployment-Name>

# Replicaaset

# StatefulSet - For Statefull app, databases

# DaemonSet - Usefull with cache
