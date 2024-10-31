HTTP header modifier
===
Use Gateway API HTTP route header modifier add new header.  
This example adds Cache-Control and My-Key to response header.
```yaml
  rules:
  - matches:
    - path:
        type: PathPrefix
        value: /
    filters:
    - type: ResponseHeaderModifier
      responseHeaderModifier:
        add:
        - name: Cache-Control
          value: "no-cache, no-store"
        - name: my-key
          value: my-value
```
Hubble visual service  
![image](https://github.com/SteveJhangOfficial/cilium-gatewayapi-example/blob/main/headermodifier/img/headermodifier-visual.png)  
  
Ref: [Gateway API header modifier](https://gateway-api.sigs.k8s.io/guides/http-header-modifier/)