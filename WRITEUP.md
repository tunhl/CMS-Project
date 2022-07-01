# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
With VW solution:
- Cost: Monthly cost, depend on size of VM: for example: B1s: $9.13; B2s: $39.71 . . .   
- Scalability: 
  + Scale up: change the size of VM
  + Scale out:  Using the service "Virtual Machine Scale Sets" for creating multiple copies and adding load balancer: using Load Balancer or Application gateway.
- Availability: SLA for VM least 95% - 99.99%
- Workflow: It could build a container or images for scaling. It could use CI/CD to build and deploy app. 

With App service solution:
- Cost: free and shared plan are for testing. Basic, Standard and Premium plans are for production workloads and run on dedicated Virtual Machine instances.  
- scalability: 
 + scale up: Get more CPU, memory, disk space, and extra features like dedicated virtual machines (VMs). Scale up by changing the pricing tier of the App Service plan
 + scale out: increase the number of VM instances that run your app. The number of instances depend on pricing tier. It could scale manually or autoscaling by rules, schedule.
- availability: SLA for app service at least 99.95% - 99.99%
- workflow: It could use CI/CD to build and deploy app service.


- *I choose App Service for deploying the app*
I choose App service solution for CMS app because it doesn't need to have a full control the VM. With current requirement, it could use app service for saving cost and time for managing operating system and installing the software for development. More over, it is more eadier for scaling.

### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.* 
I will choose VM solution if having another requirement such as:
- My application need to install the specific softwares (third parties)
- My application spend high computing -> VM is a good choice because it is cheaper.
- I want to full controll and monitor the infrastructure
