
# Kubernetes

### When someone says: "I'm running Kubernetes?"<br> 
### What does that really mean?<br> 
The following is my attempt to answer that simple question,<br>
which as you'll see, has an involved answer.<br>

[Kubernetes "Proper"](https://kubernetes.io/docs/concepts/overview/components/) is the term I use to describe the standard Kubernetes installation.<br>
Which is one or more Control Plane Node(s) and one or more Worker Node(s).<br>

### Kubernetes Control Plane Node: aka., Master Node<br>
  ### Runs: kube-apiserver, kube-controller-manager, kube-scheduler, etcd, cloud-controller-manager (OPTIONAL)<br>
### Kubernetes Worker Node: aka., Slave Node, Minion Node<br>
  ### Runs: kubelet, kube-proxy [kubeadm to join?]<br>

Kubernetes "World" is my term for all the supporting technologies surrounding Kubernetes.<br>
To get an idea of what I mean, the [CNCF Landscape](https://landscape.cncf.io/) is just a few options you have!<br>

### Can you run Kubernetes without all those supporting technologies?<br>
### The answer is NO!<br>
At minimum your need a Container Runtime (both high-level and low-level) and a CNI Plugin.<br>
Neither are include in Kubernetes Proper.<br>
And even then, you'll find that you'll need many of the other supporting technologies<br>
if you want to achieve a level of scale and performance your workload requires.<br>

### As you probably surmised by now, the meaning of<br>
### "I'm running Kubernetes?" is Kubernetes Proper + Kubernetes World<br>

So every Kubernetes installation is unique!<br>
There is no "ONE" Kubernetes installation or environment!<br>
The number of options one has explodes combinatorically.<br>
This is what makes Kubernetes "complex".<br>

I test/benchmark many different Kubernetes installations to find the<br>
best performing configuration for whatever wordload I'm considering.<br>

I call the process of describing a unique Kubernetes installation:<br>
"Describing a Kuberenetes Installation"<br>

I call the proceess of describing the results of Testing/Benchmarking a unique Kubernet installation:<br>
"Evaluating a Kuberenetes Installation"<br>

The following is only one of my personal Kubernetes installations I run on my home lab.
The answers to all these questions are specific to this single Kubernetes installation.
  Remember: Every Kubernetes installation is unique!
  Remember: There is no "ONE" Kubernetes installation or environment!


