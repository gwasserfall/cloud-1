Hosting on Azure

helm install wordpress -f wordpress-values.yaml bitnami/wordpress

helm upgrade wethink-wordpress -f wordpress-values.yaml bitnami/wordpress

# Cluster IP from nginx ingress = 102.133.132.40
kubectl get svc ingress-nginx-ingress-controller -o jsonpath="{.status.loadBalancer.ingress[0].ip}"

# Cluster adding let's encrypt cert-manager
Azure CLI used to interface with Azure Kubernetes Service (AKS)

1 node kubernetes wordpress

wethinkcube

wethinkcube-dns

1 instance scalable mysql


## Install 
helm repo add bitnami https://charts.bitnami.com/bitnami
helm install wordpress bitnami/wordpress \
  --set mariadb.enabled=false \
  --set externalDatabase.host=DATABASE-ENDPOINT \
  --set externalDatabase.user=DATABASE-USERNAME \
  --set externalDatabase.password=DATABASE-PASSWORD \
  --set externalDatabase.database=DATABASE-NAME \
  --set externalDatabase.port=3306




## Ingress Controller
helm repo add bitnami https://charts.bitnami.com/bitnami
helm install ingress bitnami/nginx-ingress-controller

## Load Balancer IP Address
kubectl get svc ingress-nginx-ingress-controller -o jsonpath="{.status.loadBalancer.ingress[0].ip}"



79 * 8

## Add the cert-manager repository, create a namespace and create CRDs:

helm repo add jetstack https://charts.jetstack.io
kubectl create namespace cert-manager
kubectl apply --validate=false -f https://github.com/jetstack/cert-manager/releases/download/v0.14.1/cert-manager.crds.yaml
 













Azure MySQL hosted, non elastic

cloud1-mysql.mysql.database.azure.com
gwasserfall@cloud1-mysql
jK3M!HoL&ty35wq5KmYs#!yq*4DD7HSVohwrK@72QnwuK7hyotgVrk7Bi6&Qd



CDN for scripts, css and images.