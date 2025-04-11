kubectl apply -f https://raw.githubusercontent.com/kubernetes/dashboard/v2.7.0/aio/deploy/recommended.yaml


kubectl create serviceaccount dashboard-admin-sa -n kubernetes-dashboard
kubectl create clusterrolebinding dashboard-admin-sa --clusterrole=cluster-admin --serviceaccount=kubernetes-dashboard:dashboard-admin-sa
kubectl create token dashboard-admin-sa -n kubernetes-dashboard


 - --namespace=kubernetes-dashboard  

        - --authentication-mode=token        # change or delete, "token" is default

        - --auto-generate-certificates       # add

        #- --enable-skip-login=true          # delete or set to false

        #- --enable-insecure-login           # delete


 spec:

  clusterIP: 10.107.176.19

  externalTrafficPolicy: Cluster   # delete

  internalTrafficPolicy: Cluster

  ports:

  - name: http

    nodePort: 32513                # delete

    port: 9090

    protocol: TCP

    targetPort: 9090

  - name: https

    nodePort: 32441                # delete

    port: 443

    protocol: TCP

    targetPort: 8443

  selector:

    k8s-app: kubernetes-dashboard

  sessionAffinity: None

  type: ClusterIP                  # change or delete

status:

  loadBalancer: {}

confirmation

➜ k run tmp --image=nginx:1.19.2 --restart=Never --rm -it -- bash

If you don't see a command prompt, try pressing enter.

root@tmp:/# curl http://kubernetes-dashboard.kubernetes-dashboard:9090

curl: (7) Failed to connect to kubernetes-dashboard.kubernetes-dashboard port 9090: Connection refused


➜ root@tmp:/# curl https://kubernetes-dashboard.kubernetes-dashboard

curl: (60) SSL certificate problem: self signed certificate

More details here: https://curl.haxx.se/docs/sslcerts.html


curl failed to verify the legitimacy of the server and therefore could not

establish a secure connection to it. To learn more about this situation and

how to fix it, please visit the web page mentioned above.


➜ root@tmp:/# curl https://kubernetes-dashboard.kubernetes-dashboard -k

curl http://192.168.100.11:32520

curl: (7) Failed to connect to 192.168.100.11 port 32520: Connection refused


➜ k -n kubernetes-dashboard get svc

NAME                        TYPE        CLUSTER-IP       ...   PORT(S)

dashboard-metrics-scraper   ClusterIP   10.111.171.247   ...   8000/TCP

kubernetes-dashboard        ClusterIP   10.100.118.128