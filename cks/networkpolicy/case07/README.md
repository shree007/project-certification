Question - Network Policy

Create a network policy called "np-restriction" to the pod "nginx-pod" in the namespace "moon"

Only allow pods to connect to the pod "nginx-pod":

    Pods in the namespace "hello" (kubectl get ns --show-labels)
    Pods with label "app:backend" in any namespace