DENY all traffic from other namespaces

Testing
$ kubectl run web --namespace=default --image=nginx --labels="app=web" --expose --port=80

$ kubectl create namespace foo
$ kubectl run test-$RANDOM --namespace=foo --rm -i -t --image=alpine -- sh
/ # wget -qO- --timeout=2 http://web.default
wget: download timed out