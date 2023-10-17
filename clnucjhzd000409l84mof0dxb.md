---
title: "Deployment and Rollout"
seoTitle: "Deployment and Rollout in Kubernates"
seoDescription: ""Master Kubernetes Deployment and Rollout strategies for seamless application management. Learn to orchestrate, scale, and roll out updates effortlessly."
datePublished: Tue Oct 17 2023 13:14:50 GMT+0000 (Coordinated Universal Time)
cuid: clnucjhzd000409l84mof0dxb
slug: deployment-and-rollout
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1697542924925/4a8730b8-2842-4b2d-b6d7-d17f3a3df187.png
tags: deployment, kubernetes, devops, devops-articles, 90daysofdevops

---

In Kubernetes, a **Deployment** is a resource object that provides a declarative way to manage applications. It's designed to handle the deployment and scaling of pods while ensuring high availability and managing updates efficiently.

### Features of Kubernetes Deployments:

1. **Pod Replica Management**: Deployments manage a set of identical pod replicas to ensure that a specified number of replicas are running at all times. If a pod fails or is terminated, the Deployment controller automatically replaces it.
    
2. **Rolling Updates**: Deployments support rolling updates, enabling you to change the configuration or update the image of your application without causing service downtime. Old pods are gradually replaced by new ones, ensuring a smooth transition.
    
3. **Rollbacks**: In the event of issues with a new version or update, Deployments allow you to easily roll back to the previous version, ensuring application stability.
    
4. **Scaling**: You can easily scale your application up or down by adjusting the number of pod replicas in the Deployment configuration. This scalability is essential for handling varying workloads.
    
5. **Declarative Configuration**: Deployments follow a declarative model. You specify the desired state (such as the number of replicas, the container image, and more) in a YAML file, and the Deployment controller takes care of ensuring that the current state matches the desired state.
    
6. **Automated Management**: Deployments abstract the complexities of managing pods. They handle the creation and deletion of pods, making it easier to manage applications.
    
7. **High Availability**: By ensuring that a specific number of pod replicas are always running, Deployments contribute to the high availability of your applications. Even in the presence of hardware failures or pod issues, the desired replica count is maintained.
    
8. **Resource Efficiency**: Deployments use a resource-efficient approach, only creating or updating the pods that need changes, rather than recreating the entire set.
    
9. **Service Integration**: Deployments are often used in conjunction with Kubernetes Services to expose and manage application access.
    

### Example of Paytm :

### ( Current Version: v10.33.1-assume we are working to upgrade to v10.33.2)

A rollout is the process of gradually deploying or upgrading your application containers.

![](https://res.cloudinary.com/practicaldev/image/fetch/s--ZW9YTW-v--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/v4airtw4m6nhhohtf08q.png align="center")

### **What happens in a deployment?**

When you first create a deployment, it triggers a rollout. A new rollout creates a new Deployment revision. Let’s call it revision 1.

![](https://res.cloudinary.com/practicaldev/image/fetch/s--ldvZNs6N--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/nh5ed7kab5zpng2tprh8.png align="center")

In the future when the application is upgraded – meaning when the container version is updated to a new one – a new rollout is triggered and a new deployment revision is created named Revision 2.

![Image description](https://res.cloudinary.com/practicaldev/image/fetch/s--ldvZNs6N--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/nh5ed7kab5zpng2tprh8.png align="center")

This helps us keep track of the changes made to our deployment and enables us to roll back to a previous version of the deployment if necessary.

* You can see the status of your rollout by running the command:
    

```plaintext
"kubectl rollout status" followed by the name of the deployment.
```

* To see the revisions and history of rollout run the command:
    

```plaintext
"kubectl rollout history" followed by the deployment name and this will show you the revisions.
```

![](https://res.cloudinary.com/practicaldev/image/fetch/s--OEtG66A2--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/4xqed7ag6z5ji41a7iwf.png align="center")

When we create a deployment, a replicaset is created and automatically the replicaset creates pods.

### Let's create a deployment:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697097682692/0301ddc3-d711-4fd6-b729-d3ad72d5ce8a.png align="center")

Here we have just changed the kind to Deployment. Other than this, most of the things are the same as replicaset.  
We have given the file name deployment.yaml.

To create the deployment we have to run the below command

```plaintext
"kubectl create -f deployment.yaml"
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697097880395/7e8ce052-8a2e-44bf-bcb8-84e85c1b51ce.png align="center")

Let's check the deployment status:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697098160950/bafc6069-fa89-4708-8ef1-cbafb24f79d2.png align="center")

It shows we have 1 deployment and 3 out of 3 ready pods. Let's check the pods

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697098173350/246b39d8-7550-4471-b088-f36976e77d0b.png align="center")

Let's check more information in the description:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697098260283/2f460aa0-dba9-4419-817d-3f00fa040701.png align="center")

Now use this command " kubectl get all" to get a few more details:

Other than the service, all of the things are related to the deployment:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697098757857/3c0225d0-391a-4f01-92f7-5d658016cc30.png align="center")

### **Deployment strategy**

1. ### Way 1 (Recreate strategy):
    
    There are two types of deployment strategies. Say for example you have 5 replicas of your web application instance deployed. One way to upgrade these to a newer version is to destroy all of these and then create newer versions of application instances.
    
    ![Image description](https://res.cloudinary.com/practicaldev/image/fetch/s--8Y34a-2R--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/c70drhxf4zcvrd8pnw0v.png align="left")
    
    This means first, destroying the 5 running instances and then deploy 5 new instances of the new application version. The problem with this as you can imagine,  
    is that during the period after the older versions are down and before any newer version is up, the application is down and inaccessible to users.
    
    [![Image description](https://res.cloudinary.com/practicaldev/image/fetch/s--s9HAVXfk--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/cq52cfqfkkgjcmu87c5x.png align="left")](https://res.cloudinary.com/practicaldev/image/fetch/s--s9HAVXfk--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/cq52cfqfkkgjcmu87c5x.png)
    
    This strategy is known as the **Recreate strategy**, and thankfully this is NOT the default deployment strategy.
    
    ![](https://res.cloudinary.com/practicaldev/image/fetch/s--Ma6xmCs5--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/q0sfn96xg5kjfxg55un8.png align="left")
    
    ![](https://res.cloudinary.com/practicaldev/image/fetch/s--6TUpiC9a--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/30kmg8gu23j68xc2z02d.png align="center")
    

### Way 2 (Rolling update by default):

1. The second strategy is were we do not destroy all of them at once. Instead, we take down the older version and bring up a newer version one by one. This way the application never goes down and the upgrade is seamless.
    
    ![Image description](https://res.cloudinary.com/practicaldev/image/fetch/s--h9wAoV_9--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/1nofohmie5ws4zx0du73.png align="center")
    
    ![Image description](https://res.cloudinary.com/practicaldev/image/fetch/s--h9wAoV_9--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/1nofohmie5ws4zx0du73.png align="center")
    
    ![Image description](https://res.cloudinary.com/practicaldev/image/fetch/s--raPCw3Ag--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/nbu068ueaz7ygtvamoiv.png align="center")
    

Note: if you do not specify a strategy while creating the deployment, it will assume it to be Rolling Update. In other words, RollingUpdate is the default Deployment Strategy.

![Image description](https://res.cloudinary.com/practicaldev/image/fetch/s--egvkNnVV--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/xzgm9hpmgjxm19u2zyd1.png align="left")

![](https://res.cloudinary.com/practicaldev/image/fetch/s--tFzDmAZ4--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/ks7cc0tn9pair79o1uhu.png align="center")

### Let's do it practically:

Let's delete our deployment thus no pods exist and we will modify our deployment and then use rollout and others here.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697184141206/c70dddf6-b38f-450e-9153-c5c0e672cbea.png align="center")

Let's update our replicas to 6

![Image description](https://res.cloudinary.com/practicaldev/image/fetch/s--xBRVOr4V--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/or6fipjzs7beuz8569w0.png align="center")

[  
](https://res.cloudinary.com/practicaldev/image/fetch/s--xBRVOr4V--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/or6fipjzs7beuz8569w0.png)Let's create the deployment, You can now check the status of deployment by watching the 6replcas (pods) getting created live :

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697184250192/f9a6b318-034f-4be6-b635-72fc1365ad62.png align="center")

Let's use the rollout status command to see the status:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697184309138/972e9487-fbf5-45f9-b65f-9f5415033996.png align="center")

Did you realize what happened?  
I guess not. Let's delete the deployment and create it fast. Then check the rollout status.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697187643724/1e81a8da-4462-45b7-9e44-cd3e683b8292.png align="center")

Let's check the history of the deployment:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697187704703/b0cc0021-044e-43f1-a857-c41336d4bf19.png align="center")

You can see that, we have just 1 revision. You can see the Cause change None as we did not set anything to record while deployment.

Let's delete the deployment and set this time.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697187845076/ca286cbb-87c2-49d9-8de3-0b5233a0c986.png align="center")

Let's create the deployment with --record command to record the Cause of change this time.

```plaintext
kubectl create -f deployment.yaml --record
```

Now, check the rollout status & history too

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697187976010/c9bd5982-22d1-45ac-bfef-7c1697dddf68.png align="center")

You can see the cause of change.

As we have used the --record command, it has recorded the command "kubectl create --filename=deployment.yaml --record=true"  
You can check the deployment information properly:

```plaintext
kubectl describe deployment myapp-deployment
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697188095687/0024e364-f5bc-4e9e-a008-65870e4dd86c.png align="center")

Let's change the image of the replica pods:

```plaintext
kubectl edit deployment myapp-deployment --record
```

we are using --record to record whatever we are doing...

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697538110228/f11f718d-72af-4317-bf71-cd871b9aec3a.png align="center")

first press "i" to get into insert mode and then change the image to nginx:1.22 which is a stable version and an older one.

In the below above, you can see the image has been changed to 1.22. We have to make sure of alignment.

Now the old pods (Which had nginx image) are terminated and new pods are created using image nginx:1.22.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697538220483/5804c040-2590-4d36-ba62-b0019bf0fd6a.png align="center")

If you type this command within a very short time, you may see something like this as in the below snippet.

```plaintext
kubectl  rollout status deployment.apps/myapp-deployment
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697538365599/7980784a-e939-454b-b88c-e53e6c347a45.png align="center")

Now check the pods or replicas;

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697538448231/157716b9-5ff8-4e14-a437-4028b3d3d250.png align="center")

They are completely new and made of ngnix:1.22 image

If you check the description of the deployment now, you can see something like this:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697547407462/90b5d2fd-65e2-420a-ac88-71b9e3aa6635.png align="center")

You can see the image has been changed to nginx:1.22 and events. Also, it is revision 2 now.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697547440560/a0a7724e-d433-444c-abe7-cea3baaf2bf8.png align="center")

Let's change the image to nginx:1.22-perl again. You may use

```plaintext
kubectl edit deployment myapp-deployment --record
OR
kubectl set image deployment myapp-deployment nginx=nginx:1.22-perl
```

Remember for this yaml file, we did set the container name as nginx and the image was set to nginx:1.22 which we are changing to nginx:1.22-perl.

We will use the below command:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697547466207/39d12611-473a-47cc-8e24-d676a2543d91.png align="center")

You can now check the rollout status:

To check the status command will be:

```plaintext
kubectl rollout status deployment.apps/myapp-deployment
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697547501809/633166b6-4438-4105-a26c-22f55581850e.png align="center")

You can see the old replicas to be terminated.

Now, you may check the history of rollouts:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697548005793/2782cf01-f7e5-4995-8684-7a5dc4ede408.png align="center")

There are a total of 3 revisions. for the 1st time, when we created the deployment, 1 rollout happened and 1 version was created.

Then we edited the image t nginx:1.22 and thus another rollout happened and a new revision appeared. Again, when we changed the image to nginx:1.22-perl, another rollout happened and another revision was created.

Now, assume that your boss told you that revision 3 was a bad decision. You should have been in revision 2, then what should you do? You can undo changes. Use this command:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697547559644/f110dce4-7ea3-45e3-8dfd-f9d77caa781b.png align="center")

This will undo revision 3 and take you back. This will create revision 4.  
Thus new pods will be created which will have image nginx:1.22

Now check out the description of the deployment and you can see the image nginx:1.22

```plaintext
kubectl describe deployment myapp-deployment
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697547590371/6e0eefe4-2c59-4fba-a84f-47f6f28013e9.png align="center")

Wait, a second. We now have 3 revisions (revision 1,3,4). Where is revision 2, Right?

```plaintext
kubectl rollout history deployment.apps\myapp-deployment
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697547623860/83adff95-1cc6-4c6c-8c2c-15fcdd3102e6.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697539179683/ca640818-b85b-4be4-9b9a-c18e2982fe2e.png align="left")

Because revision 2 the revision 4.

Hey! Did you notice that we were just applying the RollingUpdate strategy by now?[  
](https://res.cloudinary.com/practicaldev/image/fetch/s--4txM4IU0--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/jyb927xouuq85smiuyq6.png)

```plaintext
kubectl edit deployment myapp-deployment --record
```

You will find a section under spec defining strategy

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697548135943/f6ec49e9-4aea-4793-a7de-cf4e696c00c7.png align="center")

If you need to change it to Recreate or any other, you can change it to "Recreate"  
For example, for the Recreate strategy, you need to edit it to:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697548170615/a8e14e2a-d482-4fc4-80ed-92b873f27463.png align="center")

Here, we are done with this task:

Congratulations !!!

***Hope this was helpful. Thank you for your time !!***

***Stay Connected, many more to come !!***

### You can connect with me: [**https://www.linkedin.com/in/aman-srivastava-dev/**](https://www.linkedin.com/in/aman-srivastava-dev/)