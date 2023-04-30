# Creating a Kubernetes Cluster

After clone follow these steps to run this pod

1. Deploy the Dashboard UI​

```
kubectl apply -f https://raw.githubusercontent.com/kubernetes/dashboard/v2.7.0/aio/deploy/recommended.yaml
```

2. Create user

```
kubectl apply -f dashboard-adminuser.yaml
```

3. Create cluster role binding

```
kubectl apply -f cluster_role_binding.yaml
```

4. Create pod

```
kubectl apply -f createPod.yaml
```

5. Create replicaset
```
kubectl apply -f createReplicaSet
```

6. Create Deployment
```
kubectl apply -f createDeployment
```

7. Go to the below link to access the dashboard
http://localhost:8001/api/v1/namespaces/kubernetes-dashboard/services/https:kubernetesdashboard:/proxy/

8. Create a token
```
kubectl -n kubernetes-dashboard create token admin-user
```

9. Copy that token and paste that in browser

10. You will see your pod running successfully which can be seen in UI.