### 12.Kubernetes.First_deployment

## Nginx server deployment
# 00-namespace.yml
```yaml
kind: Namespace
apiVersion: v1
metadata:
  name: hw-12
  labels:
    name: hw-12
```

# 01-config-map.yml
```yaml
kind: ConfigMap 
apiVersion: v1 
metadata:
  name: nginx-configmap 
  namespace: hw-12
data:
  index.html: |
    <html>
    <h1>Welcome</h1>
    </br>
    <h1>This is a configmap Index.html </h1>
    </br>
    </html>
```
