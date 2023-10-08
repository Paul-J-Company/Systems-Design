
# Kubernetes

**When someone says: "I'm running Kubernetes?"**<br> 
**What does that really mean?**<br> 
The following is my attempt to answer that simple question,<br>
which as you'll see, has an involved answer.<br>

**[Kubernetes "Proper"](https://kubernetes.io/docs/concepts/overview/components/)** is the term I use to describe the **[standard Kubernetes installation](https://d33wubrfki0l68.cloudfront.net/2475489eaf20163ec0f54ddc1d92aa8d4c87c96b/e7c81/images/docs/components-of-kubernetes.svg)**.<br>
Which is one or more Control Plane Node(s) and one or more Worker Node(s).<br>

**Kubernetes Control Plane Node:** aka., Master Node<br>
&ensp;&ensp;**Runs:** kube-apiserver, kube-controller-manager, kube-scheduler, etcd, cloud-controller-manager (OPTIONAL)<br>
**Kubernetes Worker Node:** aka., Slave Node, Minion Node<br>
&ensp;&ensp;**Runs:** kubelet, kube-proxy [kubeadm to join?]<br>

**Kubernetes "World"** is my term for all the supporting technologies surrounding Kubernetes.<br>
To get an idea of what I mean, the [CNCF Landscape](https://landscape.cncf.io/) is just a few options you have!<br>

**Kubernetes "Platform"** is my term I use to describe all the different environments you can run Kubernetes.<br>
A very short list includes: OnPrem, Cloud, Multi-Cloud, Hybrid, Baremetal, Minikube, K3s, etc.

**Can you run Kubernetes without all those [supporting technologies](https://landscape.cncf.io/)?**<br>
**The answer is NO!**<br>
At minimum you need a Container Runtime (both high-level and low-level) and a CNI Plugin.<br>
Neither are include in Kubernetes Proper.<br>
And even then, you'll find that you'll need many of the other supporting technologies<br>
if you want to achieve a level of scale, performance, and maintainability your workload requires.<br>
In other words,<br>
you'll need many of the other supporting technologies to achieve the desired [System Properties](https://github.com/Paul-J-Company/Systems-Design/blob/main/Systems-Design.md#system-properties).

As you probably surmised by now, the meaning of<br>
**"I'm running Kubernetes?" is Kubernetes Proper + Kubernetes World running on one or more different Kubernetes Platforms**<br>

**Kubernetes "Installation"** is my term I use to describe a unique installation of kubernetes<br>
comprised of Kubernetes Proper + Kubernetes World running on one or more different Kubernetes Platforms.<br>

So every Kubernetes installation is unique!<br>
There is no "ONE" Kubernetes installation, environment or platform!<br>
The number of options one has explodes combinatorically.<br>
This is what makes Kubernetes "complex".<br>

I call the process of describing a unique Kubernetes installation:<br>
**"Describing a Kuberenetes Installation"**<br>

I then test/benchmark many different Kubernetes installations to find<br>
the best performing configuration for whatever workload I'm considering.<br>

I call the process of describing the results of Testing/Benchmarking a unique Kubernet installation:<br>
**"Evaluating a Kuberenetes Installation"**<br>

The following is a list of Kubernetes installations I've implemented on my home lab.

Each instance is specific to a single Kubernetes installation.<br>
&ensp;&ensp;Remember: **Every Kubernetes installation is unique!**<br>
&ensp;&ensp;Remember: **There is no "ONE" Kubernetes installation or environment!**<br>

Each instance has an accompanying Youtube video that shows the details of<br>
how I implemented the unique Kubernetes installation and how I evaluated it.<br>

(NOT DONE YET, EXAMPLES COMING SOON)<br>



