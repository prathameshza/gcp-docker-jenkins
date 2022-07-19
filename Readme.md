A simple devops project to demonstrate the use of Docker and jenkins with the help of GCP compute engine.



![GCP Docker Jenkins](https://user-images.githubusercontent.com/46810093/178714430-4523e397-0ac2-4a96-90b7-6102fbb1dd9b.svg)


In this project we will create a flask web app and use docker to containerize it and deploy to gcp compute instance with the help of jenkins.

First run your app localy
![appoff2](https://user-images.githubusercontent.com/46810093/179789759-c9a26ae8-44f1-4ff2-974d-f83551485477.png)
![appoff1](https://user-images.githubusercontent.com/46810093/179789770-f2b390ae-9397-4f56-8b45-2fdcb34107c7.png)


Create a Dockerfile with debian os and gunicorn module

Then upload it to github repo with git and gh cli

![upload](https://user-images.githubusercontent.com/46810093/179790341-7bdc05c9-4700-46d1-a953-b96273887198.png)


we will create our compute instance in the gcp cloud and deploy jenkins over it

make sure to allow network firewall rule for http protocol

after that install docker and push your image to docker hub

![basic instance](https://user-images.githubusercontent.com/46810093/179791012-226ca759-af87-4315-b870-ac30bd5d66ae.png)


after that we will launch the jenkins to port 8080 and creat a simple freestype project

the configuration will look like this

![jenkins config](https://user-images.githubusercontent.com/46810093/179792390-5527afd9-e851-4ae1-af12-a28d01996512.png)
![console out](https://user-images.githubusercontent.com/46810093/179792617-9ab550b1-aac9-42a2-878a-5d71570950a4.png)

after the build started we can launch our app on http://[ExternalIPofVm]:[Your app Port]

![apponline](https://user-images.githubusercontent.com/46810093/179793118-927a022d-a8c6-4ec6-a06e-b7ab3e3428b3.png)

