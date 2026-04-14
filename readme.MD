# ingress controller

REGION_CODE=us-east-1
CLUSTER_NAME=expense
ACC_ID=805160322688


### PERMISSIONS

1 .OIDC provider 
...
eksctl utils associate-iam-oidc-provider \
    --region $REGION_CODE \
    --cluster $CLUSTER_NAME \
    --approve



#########  to check authentication 

kubectl get configmap aws-auth -n kube-system -o yaml



########   for other user can able to check cluster access
    aws eks update-kubeconfig --region us-east-1 --name expense