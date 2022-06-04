<!-- @format -->

# Load Balancer

Help to identify the Port , the loadBalancer forward the traffic to the port in the cluster that connect to a specific service. And this service use the label to connect the pods blue and green

This will happend the same if we have a nother service, we will give it a service of type LoadBalancer, that service will have a separate loadbalancer, with a separate public IP

# Proxy

Allow was redirect traffic base on his path, to do authentication, to set cors headers, etc. --> Application level operations HTTP aplication layer protocol -> Layer 7

First Class that desribe ingres rules for http traffic, resources that describe this path based routing

## HTTP revere proxy - Ingress Controller

Configure this

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

# Type ClusterIP

allow connection inside the Cluster between the pods

```yaml
spec:
  type: ClusterIP
  ports:
    - port: 80
      targetPort: 8080
```

# Type NodePort

```yaml
spec:
  type: NodePort
  ports:
    - port: 80
      targetPort: 8080
```
