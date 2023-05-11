## CMPE 172 - Lab #10 Notes

### CI Workflow (Part 1)
- Create my public repo which is name spring-gumball
![image desc](./screenshot/1.png)<br><br>

- After creating repo, upload provide code into my repo

- Go to actions option, choose new workflow by configure "java with Gradle"
![image desc](./screenshot/1.1.png)<br><br>

- Then it will generate the file in the .github/gradle.yam

- In deployment.yaml, change replicas into 2, insteads of 4

- After that, click on the process and check the code which is running through CI

- Screenshot after builing succesful
![image desc](./screenshot/2.2.png)<br><br>

### CD Workflow (Part 2)
- Set up the project and cluster
![image desc](./screenshot/3.png)<br><br>

- Next is enabling the container register and google kubernetes engine API
![image desc](./screenshot/4.png)<br><br>

- Go to IAM, choose service account options, then create a new service and generate new key
![image desc](./screenshot/6.png)
![image desc](./screenshot/5.png)<br><br>

- Then add add grant access for spring-gumball service : Kubernetes engine developer and storage admin
![image desc](./screenshot/7.png)<br><br>

- Same as CI workflow, I Go to actions option, choose new workflow by configure "Build and Deploy to GKE"
![image desc](./screenshot/7.1.png)<br><br>

- Then it will generate the file in the .github/google.yaml

- Change the name of project ID and cluster in google.yaml file

- Then go to setting option, add key which I generate in spring-gumball service and GKE_PROJECT ID
![image desc](./screenshot/9.png)
![image desc](./screenshot/8.png)<br><br>

- Trigger a CD deployment by creating a new 2.3 gitHub release
![image desc](./screenshot/10.png)
![image desc](./screenshot/11.png)
![image desc](./screenshot/12.png)
![image desc](./screenshot/13.png)<br><br>

- Then creating Kubernetes ingress, named spring-gumball lb, choose spring-gumball-service for backends, http port is set as 80
![image desc](./screenshot/14.png)
![image desc](./screenshot/15.png)
![image desc](./screenshot/16.png)
![image desc](./screenshot/17.png)<br><br>

- Creating Kubernetes ingress sucessfully
![image desc](./screenshot/18.png)<br><br>

- Check workload, service, ingress, load balancer, everything look good.
![image desc](./screenshot/22.png)
![image desc](./screenshot/20.png)
![image desc](./screenshot/21.png)<br><br>

- Display spring-gumball page
![image desc](./screenshot/19.png)<br><br>






