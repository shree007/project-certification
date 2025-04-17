1. create namespace red and blue.

user jane can only get secrets in namespace red.

user jane can only get and list secrets in namespace blue.

test it using auth can-i.

solution:

kubectl create role janerole --verb=get.list --resource=secret -n blue
kubectl create role janerole --verb=get --resource=secret -n red
kubectl create rolebinding janerolebinding --role=janerole --user=jane -n blue
kubectl create rolebinding janerolebinding --role=janerole --user=jane -n red

test:
kubectl auth can-i get secrets -n blue --as=jane -n blue
kubectl auth can-i get secrets -n blue --as=jane -n red

2. create a clusterrole deploy-delete which allows to delete deployments

user jane can delete deployments in all namespaces

user jim can delete deployments in red namespace

Test it using kubectl auth can-i

solution:

kubectl create clusterrole deploy-deleter --verb=delete --resource=deployments
kubectl create clusterrolebinding deploy-deleter 
kubectl create clusterrolebinding deploy-deleter --clusterrole=deploy-deleter --user=jane

kubectl create rolebinding deploy-deleter --clusterrole=deploy-deleter --user=jim -n red