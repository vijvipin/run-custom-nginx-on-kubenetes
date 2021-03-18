# run-custom-nginx-on-kubenetes

## What: A simple kubernetes deployment to show how can you run your own customer nginx image using kubernetes. Here - [my-nginx-custom-image] , I took nginx:latest image as a base then hosted my two simple HTML pages on this, dockerized it.

So this example show you " How can you run your own customer images from docker.hub on kubenetes.

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

  
This tells us the port 32601 on which the nginx is listening now: Now open: http://localhost:32601/

## Here you are: Your very own nginx running on kubenetes.



[my-nginx-custom-image]: https://hub.docker.com/r/vijvipin/simple-nginx-webpage
