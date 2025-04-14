kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.10.1/deploy/static/provider/cloud/deploy.yaml

kubectl run pod1 --image=nginx
kubectl run pod2 --image=httpd
kubectl expose pod pod1 --port=80 --name service1
kubectl expose pod pod2 --port=80 --name service2


TLS:


curl -k https://10.98.127.132:443

curl -vk https://10.98.127.132:443


curl -vk https://10.98.127.132:443/service1
curl -vk https://10.98.127.132:443/service2

*  subject: O=Acme Co; CN=Kubernetes Ingress Controller Fake Certificate

create self signed certificate
openssl req -x509 -newkey rsa:4096 -keyout key.pem -out cert.pem -days 365 -nodes

kubectl create secret tls tls-secret --cert=cert.pem --key=key.pem

kubectl apply -f tls.yaml

curl -vk https://secure-ingress.com/service2 --resolve secure-ingress.com:443:10.98.127.132
it is working