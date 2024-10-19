HTTP traffic splitting
===
Use Gateway API HTTP route specify weights to shift traffic between different backends.
```yaml
  rules:
  - matches:
    - path:
        type: PathPrefix
        value: /
    backendRefs:
    - name: http-traffic-splitting-svc-v1
      port: 80
      weight: 90
    - name: http-traffic-splitting-svc-v2
      port: 80
      weight: 10
```