# Observability


## Send gRPC request
```
cd api/protobuf/blog/v1

grpcurl -plaintext -proto ./blog.proto -d '{"username": "jack", "password": "123456"}' localhost:80 api.protobuf.blog.v1.BlogService/SignUp
```


## Observability
```
暴露 prometheus 服务的端口
kubectl port-forward svc/prometheus 9090:9090 -n istio-system

暴露 grafana 服务的端口
kubectl port-forward svc/grafana 3000:3000 -n istio-system

暴露 kiali 服务的端口
kubectl port-forward svc/kiali 20001:20001 -n istio-system

暴露 jeager-query 服务的端口
kubectl port-forward svc/tracing 8080:80 -n istio-system
```
