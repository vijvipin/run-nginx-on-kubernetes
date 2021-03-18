# run-nginx-on-kubernetes
A simple kubernetes deployment to show how can you run nginx:latest image using kubernetes.

Take following two steps [On windows Machine]
1. First put both these files in a folder on your machine.
2. Open CMD and move to this folder and run follwoing two KUBECTL commands

`
$ kubectl apply -f dep.yaml
$ kubectl apply -f service.yaml
`

The first command will create a deployment and the second create a serivce to access this deployment. Now

`
$ kubectl get all
`
The above command will show you all things deployed. Check out the image. We see a service with name nginx.

![image](https://user-images.githubusercontent.com/45314106/111628312-6026fa00-87f0-11eb-89f3-573de0136958.png)


NAME                   TYPE        CLUSTER-IP     EXTERNAL-IP   PORT(S)        AGE
service/nginx          NodePort    10.110.5.130   <none>        80:31427/TCP   4m19s
  
This tells us the port 31427 on which the nginx is listening now: Now open: http://localhost:31427/

Here you are: Your very own nginx running on kubenetes.
