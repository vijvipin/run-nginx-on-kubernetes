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
The above command will show you all things deployed. CHeck out the image

![image](https://user-images.githubusercontent.com/45314106/111628312-6026fa00-87f0-11eb-89f3-573de0136958.png)
