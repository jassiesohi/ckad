

# Commands reference for CKAD


# check if the app is running in the pod
kubectl exec -it webapp-color --sh
nc -v -z -w 2 10.0.0.$i 80

# Delete the pods with labels
kubectl delete po -l app=webapp-color # example
kubectl delete po -l name=webapp-color # example


# export running pod configuration to yaml file
kubectl get po -l app=webapp-color -oyaml > webapp-color.yaml # example
kubectl get po nginx -oyaml > nginx.yaml # example


 # force delete the pod with instantly
 kubectl delete po -l app=webapp-color --grace-period=0 -force # example
 kubectl replace -f webapp-color.yaml --force --grace-period=0 # example



