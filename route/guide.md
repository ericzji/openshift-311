## Create container f5-demo-app-route
```
oc project f5demo
oc create -f f5-cluster-deployment.yaml
oc create -f f5-demo-app-route-deployment.yaml -n f5demo
oc create -f f5-demo-app-route-route.yaml -n f5demo
```

## Delete container f5-demo-app-route
```
oc delete -f f5-demo-app-route-deployment.yaml -n f5demo
oc delete -f f5-demo-app-route-route.yaml -n f5demo
oc scale --replicas=10 deployment/f5-demo-app-route -n f5demo
```