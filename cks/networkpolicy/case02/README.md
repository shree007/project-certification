Allow only selected application to communicate with destinated application


Deploy Application A, B and C
$ kubectl run appA --image=nginx --labels="app=applicationA" --expose --port=80

$ kubectl run appB --image=nginx --labels="app=applicationB" --expose --port=80

$ kubectl run appC --image=nginx --labels="app=applicationC" --expose --port=80

