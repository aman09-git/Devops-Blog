---
title: "Pods in Kubernates with Yaml"
seoTitle: "Pods in Kubernates with Yaml"
seoDescription: ""Learn Kubernetes Pods: Essential building blocks. YAML configurations for scalable and resilient containerized applications. Deploy, manage, and optimize P"
datePublished: Thu Sep 28 2023 12:04:20 GMT+0000 (Coordinated Universal Time)
cuid: cln34nnzm00050aic6crc7vs9
slug: pods-in-kubernates-with-yaml
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1695902449550/893993f6-18ef-4823-be0f-d6d313b65e4a.jpeg
tags: kubernetes, devops, devops-articles, 90daysofdevops, pods

---

### **What is a Pod in Kubernetes?**

Pods are the smallest deployable units in Kubernetes. A Pod represents a single instance of a running process or a group of tightly coupled processes running together on a single node. While containers are commonly used within Pods, Pods can also include multiple containers that share resources and network connectivity.

The purpose of a Pod is to provide a cohesive and isolated environment for containers to run and share resources, including storage, network, and inter-process communication. Containers within a Pod can communicate with each other via [localhost](http://localhost), as they share the same network namespace.

### **Key Characteristics of Pods:**

* **Single or multiple containers within a Pod:** Pods can contain one or more containers that are scheduled and deployed together on the same node.
    
* **Shared network namespace:** Containers in a Pod share the same network namespace, allowing them to communicate using [localhost](http://localhost).
    
* **Shared storage and volumes:** Pods can share storage volumes, allowing data sharing and persistence between containers within the same Pod.
    

### Single Node K8 cluster:

Containers in the pods are coupled within the node, and if the number of users increases then we have to increase the number of pods in the nodes and if the pod capacity has reached its maximum then we have to create a new container pod with a new node.

Pods usually have one on one relationship with the container.

![CKA & CKAD Series (Part 3): Replication controller &  replicaset_kubernetes_weixin_0010034-K8S/Kubernetes](https://res.cloudinary.com/practicaldev/image/fetch/s--OF9vIlbI--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/0ljj7bpx7lxzz5d0re41.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1695898749196/8bb71d98-1c08-4771-8da7-016b7dad17b6.png align="center")

### Multi-Cluster node:

A single pod can have multiple containers until and unless they all are not same. We can have additional pods as helper containers to support tasks, like processing user data.

In that kind of scenario, we have the application container with the support container in the same pod. Support container will be created with the application container and die with the same.

Also, the application container and support container share the same network and storage.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1695902065365/f5fd8b1d-63d5-4134-8fd9-9030444d7ebc.png align="center")

### YAML:

In YAML, we keep things in **Key: value** format

![Image description](https://res.cloudinary.com/practicaldev/image/fetch/s--7uKwjPrx--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/gzfdxdanja86utykqyss.png align="center")

here keys are Fruit, Vegetable etc. & values are Apple, Carrot etc.

Also, this is how the array & dictionary is placed in YAML:

![Image description](https://res.cloudinary.com/practicaldev/image/fetch/s---LGxuMK9--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/bs1y1lmsyc71s154ekbu.png align="center")

Note: You need to make sure the gaps are formatted well.

Also, you may have a mix-up of all of these:

![Image description](https://res.cloudinary.com/practicaldev/image/fetch/s--_5Whr_iI--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/m7mjzxo64su934z2x61k.png align="center")

Let's check an example where we can use YAML to represent one

Example 1:

[![Image description](https://res.cloudinary.com/practicaldev/image/fetch/s--kHVAMVB2--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/6muw9czp4055jngc5jk3.png align="left")](https://res.cloudinary.com/practicaldev/image/fetch/s--kHVAMVB2--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/6muw9czp4055jngc5jk3.png)

You can see the key's color, model, transmission & price. All of them had their different values. Even the model is not a key here. Rather a dictionary which has keys Name & Year in it.

So, this is how we use YAML.

Example 2:

[![Image description](https://res.cloudinary.com/practicaldev/image/fetch/s--KCK_B1RW--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/2y1o2rltjwya7dnwuf8c.png align="left")](https://res.cloudinary.com/practicaldev/image/fetch/s--KCK_B1RW--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/2y1o2rltjwya7dnwuf8c.png)

Here we we have added all the car's names with colors in the list format.

But when we would like to have every detail of them, we will use dictionary format here. Like this

[![Image description](https://res.cloudinary.com/practicaldev/image/fetch/s--mUebmiEs--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/o9n6fiaosi962symddof.png align="left")](https://res.cloudinary.com/practicaldev/image/fetch/s--mUebmiEs--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/o9n6fiaosi962symddof.png)

and this is a list of dictionaries.

### **Let's create a pod using the YAML file**

Let's create a file called pods-definition.yaml

[![Image description](https://res.cloudinary.com/practicaldev/image/fetch/s--B-b5i5zE--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/g8ms3ojtnhuw7p6dsgrf.png align="center")](https://res.cloudinary.com/practicaldev/image/fetch/s--B-b5i5zE--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/g8ms3ojtnhuw7p6dsgrf.png)

For a pod, we must have these contents. There might be different values for different things but for our purpose, we will just use this one.

[![Image description](https://res.cloudinary.com/practicaldev/image/fetch/s--AornchU---/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/5uaoshkb4raqv55nmain.png align="center")](https://res.cloudinary.com/practicaldev/image/fetch/s--AornchU---/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/5uaoshkb4raqv55nmain.png)

We will use the apiVersion as V1 for now.

[![Image description](https://res.cloudinary.com/practicaldev/image/fetch/s--218M9Vfu--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/lku0i6cqe3tyd26lsv0k.png align="center")](https://res.cloudinary.com/practicaldev/image/fetch/s--218M9Vfu--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/lku0i6cqe3tyd26lsv0k.png)

For the kind, we will use "pod" as we are creating a pod.

[![Image description](https://res.cloudinary.com/practicaldev/image/fetch/s--mzyAOT6E--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/6g9dkefvu8mgtc1gwmum.png align="center")](https://res.cloudinary.com/practicaldev/image/fetch/s--mzyAOT6E--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/6g9dkefvu8mgtc1gwmum.png)

The metadata, provides data about the object, in our case object is a pod. we are going to provide additional information like the name of the pod and labels we want to add so that we can filter later among many many pods to find this one.

[![Image description](https://res.cloudinary.com/practicaldev/image/fetch/s--RnCX8pQu--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/xxhii1arr18pzs1kxmzj.png align="center")](https://res.cloudinary.com/practicaldev/image/fetch/s--RnCX8pQu--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/xxhii1arr18pzs1kxmzj.png)

Look, there are strings for some values and dictionaries for some.

[![Image description](https://res.cloudinary.com/practicaldev/image/fetch/s--3E-Wqx5z--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/c3382mmbnzr3mq1iyqke.png align="center")](https://res.cloudinary.com/practicaldev/image/fetch/s--3E-Wqx5z--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/c3382mmbnzr3mq1iyqke.png)

You can also add additional information for labels:

[![Image description](https://res.cloudinary.com/practicaldev/image/fetch/s--JkSJyYXL--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/apr2yoz2p2zasbwkiwh7.png align="center")](https://res.cloudinary.com/practicaldev/image/fetch/s--JkSJyYXL--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/apr2yoz2p2zasbwkiwh7.png)

Now, let's check the spec one:

Here we are going to set the containers list etc. For this pod, we just want 1 container to be created. We are going to use the "nginx" image with "nginx-container" as the name of the container.  
We have formatted it in list format. Because there might be several containers in a pod.

[![Image description](https://res.cloudinary.com/practicaldev/image/fetch/s--rI1PK6sQ--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/47k1orr5736kywsycxzu.png align="center")](https://res.cloudinary.com/practicaldev/image/fetch/s--rI1PK6sQ--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/47k1orr5736kywsycxzu.png)

[![Image description](https://res.cloudinary.com/practicaldev/image/fetch/s--YgJMuv0c--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/xbl80zbqdel1va75klkl.png align="center")](https://res.cloudinary.com/practicaldev/image/fetch/s--YgJMuv0c--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/xbl80zbqdel1va75klkl.png)

Also, we can have additional information for a container like resources, ports etc.

[![Image description](https://res.cloudinary.com/practicaldev/image/fetch/s--jBojykB2--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/27vl0zu00cwry8zz0ijr.png align="center")](https://res.cloudinary.com/practicaldev/image/fetch/s--jBojykB2--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/27vl0zu00cwry8zz0ijr.png)

Now let's create a pod. For that, use these codes:

[![Image description](https://res.cloudinary.com/practicaldev/image/fetch/s--BiNYbmm2--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/mtvf9t9s7t28g76qrhnk.png align="center")](https://res.cloudinary.com/practicaldev/image/fetch/s--BiNYbmm2--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/mtvf9t9s7t28g76qrhnk.png)

```plaintext
apiVersion: v1
kind: Pod
metadata:
  name: myapp-pod1
  labels:
    name: myapp1
spec:
  containers:
  - name: nginx-container
    image: nginx
```

To create the pod go with the below command:

```plaintext
kubectl apply -f pod.yml
```

We have used -f to force it to use pod.yml to create a pod using the apply command.

You can check the pod using:

```plaintext
kubectl get pods
```

Also to know more about a particular pod, you can use this command :

"kubectl describe pod "

```plaintext
kubectl describe pod myapp-pod1
```

You can delete the pod using "kubectl delete pod "

```plaintext
kubectl delete pod myaap-pod
```

And then check if it is available or not:

```plaintext
kubectl get pods
```

### Few more commands that will be useful:

```plaintext
kubectl get pods -o wide: To check on which node pods are placed 
kubectl run —help : This will help you in many ways 
```