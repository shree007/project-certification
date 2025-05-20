Create a service account named "seminar-sa" on the namespace "seminar"

Create a new role named "k8s-seminar" in the namespace "seminar" which only allows "create and update" operations only on resources of type "pods" and "deployments"

Create a new rolebinding name "k8s-seminar-bind" binding to the newly created role to the service account created previously named "seminar-sa".