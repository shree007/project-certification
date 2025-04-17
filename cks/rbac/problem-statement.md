create namespace red and blue.

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