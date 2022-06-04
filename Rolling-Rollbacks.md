<!-- @format -->

# Rolling - Rollbacks

Allow us to exchanges the pods, one is down and one is up.

```yaml
strategy:
  rollingUpdate:
    maxSurge: 1
    maxUnavailable: 0
```
