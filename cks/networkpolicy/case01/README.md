Deny every application to Ingress

$ kubectl run web --image=nginx --labels="app=web" --expose --port=80


$ kubectl run --rm -i -t --image=alpine test-$RANDOM -- sh

![Deny All](deny-all.png)
