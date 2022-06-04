<!-- @format -->

# Read Logs

You can only read the logs of a pod

k logs <podName>

# Read Logs by Label selector

k logs -l <label=labelName>
k logs -l app=blue-green
k logs -l colour=blue

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
