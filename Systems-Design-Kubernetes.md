
# [Kubernetes](https://miro.medium.com/v2/resize:fit:1400/format:webp/0*-GmCgKeebCe9AMjW.png)

I recommend viewing the corresponding [YouTube Playlist](https://www.youtube.com/@PaulJCompany/playlists) for this page.<br>
You can also jump down to the end of this page to review the [Visualizing Kubernetes](https://github.com/Paul-J-Company/Systems-Design/blob/main/Systems-Design-Kubernetes.md#visualizing-kubernetes) or [Additional Resources](https://github.com/Paul-J-Company/Systems-Design/blob/main/Systems-Design-Kubernetes.md#additional-resources) section.<br>

**When someone says: "I'm running Kubernetes?"**<br> 
**What does that really mean?**<br> 
The following is my attempt to answer that simple question,<br>
which as you'll see, has an involved answer.<br>

**[Kubernetes "Proper"](https://kubernetes.io/docs/concepts/overview/components/)** is the term I use to describe the **[standard Kubernetes installation](https://d33wubrfki0l68.cloudfront.net/2475489eaf20163ec0f54ddc1d92aa8d4c87c96b/e7c81/images/docs/components-of-kubernetes.svg)**.<br>
Which is one or more Control Plane Node(s) and one or more Worker Node(s).<br>

**Kubernetes Control Plane Node:** aka., Master Node<br>
&ensp;&ensp;**Runs:** kube-apiserver, kube-controller-manager, kube-scheduler, etcd, cloud-controller-manager (OPTIONAL)<br>
**Kubernetes Worker Node:** aka., Slave Node, Minion Node<br>
&ensp;&ensp;**Runs:** kubelet, kube-proxy [kubeadm to join as one option]<br>

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
The number of options one has [explodes combinatorically](https://en.wikipedia.org/wiki/Combinatorial_explosion).<br>
This is what makes Kubernetes "complex".<br>

I call the process of describing a unique Kubernetes installation:<br>
**"Describing a Kuberenetes Installation"**<br>

I then test/benchmark many different Kubernetes installations to find<br>
the best performing configuration for whatever workload I'm considering.<br>

I call the process of describing the results of Testing/Benchmarking a unique Kubernet installation:<br>
**"Evaluating a Kuberenetes Installation"**<br>

## Example Kubernetes Installations
The following is a list of Kubernetes installations I've implemented on my home lab.

Each instance is specific to a single Kubernetes installation.<br>
&ensp;&ensp;Remember: **Every Kubernetes installation is unique!**<br>
&ensp;&ensp;Remember: **There is no "ONE" Kubernetes installation or environment!**<br>

Each instance has an [accompanying Youtube video](https://www.youtube.com/@PaulJCompany/) that shows the details of<br>
how I implemented the unique Kubernetes installation and how I evaluated it.<br>

(NOT DONE YET, EXAMPLES COMING SOON)<br>

## Visualizing Kubernetes
[Tools to Visualize Kubernetes:](https://github.com/collabnix/kubetools) [[1]](https://kubeview.benco.io/) [[2]](https://steampipe.io/blog/k8s-insights) [[3]](https://dev.to/ajeetraina/10-kubernetes-visualization-tool-that-you-cant-afford-to-miss-414k) [[4]](https://www.infoworld.com/article/3488817/15-tools-that-make-kubernetes-easier.html) [[5]](https://learnk8s.io/visualise-dependencies-kubernetes) [[6]](https://github.com/spekt8/spekt8) [[7]](https://collabnix.com/exploring-cluster-resources-with-kubeview-a-visual-approach-to-kubernetes-monitoring/) [[8]](https://github.com/oslabs-beta/indiK8or) [[9]](https://github.com/datacenter/ACI-Kubernetes-Visualiser) [[10]](https://github.com/vasu1124/k8s-visualizer) [[11]](https://github.com/intelops/kubviz) [[12]](https://github.com/steveteuber/kubectl-graph) [[13]](https://github.com/joatmon08/kubernetes-demo) [[14]](https://github.com/linchpiner/kubegraph) [[15]](https://github.com/Jont828/cluster-api-visualizer) [[16]](https://github.com/stepanstipl/k8s-viz) [[17]](https://github.com/mjbright/kubeview) [[18]](https://github.com/topics/kubernetes-visualization) [[19]](https://github.com/Shopify/kubepacity) [[20]](https://github.com/oslabs-beta/Allok8) [[21]](https://github.com/n3wscott/graph) [[22]](https://github.com/salesforce/sloop) [[23]](https://github.com/kubernetes-sigs/cluster-api/issues/2916) [[24]](https://github.com/Azure/azure-kubernetes-visualizer) [[25]](https://github.com/chiradeep/qube-viz) [[26]](https://github.com/oslabs-beta/ClusterWatch)<br>
[How to Convert Any Text Into a Graph of Concepts](https://towardsdatascience.com/how-to-convert-any-text-into-a-graph-of-concepts-110844f22a1a)<br>

[Visualizing 10 Common Statistical Concepts of Data Science](https://towardsdev.com/diagrams-for-10-common-concepts-of-data-science-bbc79cd753f6) [[1]](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*KGB62_1stkcg9erYWQk8sw.png) [[2]](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*huUr4hGOedKFFPcVUg1zaA.png) [[3]](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*5eCQHaWzSKgSbehxWzzvpw.png) [[4]](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*wv8VZJy691LPSvX_TT32dA.png) [[5]](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*F6TggVdQyB9FaRhvJLtJ-g.png) [[6]](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*bvc18HBTqULk021KJgp-tw.png) [[7]](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*2bQKzOTNO7iv1KPkaT1Sog.png) [[8]](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*f8POEKDgVx3nVIF9RFOohg.png) [[9]](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*16VQ1ZzNFy8gXMT7a8TIgA.png) [[10]](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*YW9rFvihc3gRazMkQGKZdg.png) [[11]](https://miro.medium.com/v2/resize:fit:1384/format:webp/1*gwGoctimCF5iirqJMsLYAg.png) [[12]](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*Z9lJw2SydDdUdnCcV4eOIw.png) [[13]](https://miro.medium.com/v2/resize:fit:1380/format:webp/1*DrP23Bx_nNBTgoMhN1sJGQ.png) [[14]](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*w40PcBdM7ykYZTcG2UV08g.png) [[15]](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*uSmjQSwiTdzetma81xYbKw.png) [[16]](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*fbzbmojqwF1UCjkGozXVnQ.png) [[17]](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*p8HPlBv6OHms2bSinmwA4Q.png) [[18]](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*wtcKpVKur5sRoJY2xsLDqg.png) [[19]](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*SO4k-HC9t2tMhYwD0ijJnA.png)<br>

[Visualizing CNCF Technical Advisory Groups](https://miro.medium.com/v2/resize:fit:2000/format:webp/1*vybpMui4AHBrx-pJABbOKQ.png) [[1]](https://devstats.cncf.io/)<br>
[Visualizing CNCF Landscapes](https://landscape.cncf.io/) [[1]](https://landscapes.dev/) [[2]](https://landscape.lfai.foundation/) [[3]](https://landscape.openssf.org/)<br>
[CNCF Platforms White Paper](https://tag-app-delivery.cncf.io/whitepapers/platforms/)<br>
[Visualizing CNCF Platforms White Paper](https://miro.medium.com/v2/resize:fit:1400/format:webp/0*uLZkzTWyXlM-prhb.png)<br>
[Visualizing Hierarchy of AppDeveloper Needs from KubeCON NA 2023](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*Z6ucBR_3RJ5YL7EM7fEzMQ.jpeg) [[1]](https://medium.com/vedcraft/key-takeaways-from-kubecon-cloudnativecon-north-america-2023-86219684f2d9)<br>
[Visualizing APIs for solving distributed application challenges](https://github.com/salaboy/dapr-testcontainers/blob/main/imgs/dapr-components.png) [[1]](https://miro.medium.com/v2/resize:fit:2000/format:webp/0*uX4rvt0DHPQxH0sK)<br>
[Visualizing OWASP Top 10 LLM Applications](https://llmtop10.com/) [[1]](https://miro.medium.com/v2/resize:fit:1400/format:webp/0*8GG8RfUkKE3p2ym0)<br>
     
[Visualizing DevOps](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*8nimBWvKbst1nmTnuPv-wA.jpeg) [[1]](https://cloudmize.medium.com/top-devops-tools-for-2024-essential-software-for-streamlined-software-development-91bc88a995d2)<br>
[Visualizing DevOps in Different Environments](https://github.com/metaleapca) [[1]](https://github.com/metaleapca/metaleap-devops-in-k8s/blob/main/metaleap-devops-in-k8s.pdf)<br>
[Visualizing DevOps in Kubernetes](https://github.com/metaleapca/metaleap-devops-in-k8s/blob/main/metaleap-devops-in-k8s.pdf) [[1]](https://blog.devgenius.io/devops-in-k8s-pod-lifecycle-part-one-c5c78d9da941)<br>
[Visualizing DevOps in Linux](https://github.com/metaleapca/metaleap-devops-in-linux/blob/main/metaleap-devops-in-linux.pdf)<br>
[Visualizing DevOps K8s Tools](https://github.com/metaleapca/metaleap-k8s-tools/blob/main/metaleap-k8s-tools.pdf)<br>
[Visualizing DevOps with Terraform](https://github.com/metaleapca/metaleap-devops-in-terraform/blob/main/metaleap-devops-in-terraform.pdf)<br>
[Visualizing DevOps with ArgoCD](https://github.com/metaleapca/metaleap-devops-in-argocd/blob/main/metaleap-devops-in-argocd.pdf)<br>

[Visualizing GitOps with Argo & Jenkins](https://miro.medium.com/v2/resize:fit:1100/format:webp/1*aFrAvtOtsQAR9ZFZlTtlPA.png) [[1]](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*E5TUjGfs0CrZTU6QB5pXXg.png) [[2]](https://medium.com/@emrah-t/extending-your-ci-cd-pipeline-with-gitops-an-end-to-end-automation-with-argocd-and-jenkins-on-b456a8760a11)<br>

[Visualizing Methodology for Building Software-as-a-Service Apps](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*xj8exAVC0kguMgyYltDapg.png) [[1]](https://medium.com/@tech_18484/introduction-701b7a8f4730) [[2]](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*QPTyF4ejabd1db3F6hl9Mg.png) [[3]](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*ZoYX6WbQEbVWL1i6zylpkQ.png) [[4]](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*UBvkj-wYqEp_pimuzqnQ8w.png)<br>
    
[Visualizing Lean Platform Engineering with Azure](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*jQms01KS7IDTAC3u-AUCdQ.gif) [[1]](https://medium.com/@artem_lajko/lean-platform-engineering-0509afceaf82)<br>

[Visualizing Azure Application Gateway for Containers](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*IPHLDIJRYVDt4wRgpW_SkQ.gif) [[1]](https://medium.com/@muthanagavamsi/azure-application-gateway-for-containers-66920f18659)<br>
       
[What are the Differences Between VPA, HPA, CA, and CPA in Kubernetes?](https://hwchiu.medium.com/what-are-the-differences-between-vpa-hpa-ca-and-cpa-in-kubernetes-5f74c97001ed)<br>
[Visualizing VPA, HPA, CA, and CPA in Kubernetes](https://miro.medium.com/v2/resize:fit:1400/format:webp/0*hXlG9FTm02CrdyR_.png)<br>

[Visualizing Kubernetes Troubleshooting Mindmap](https://github.com/metaleapca/metaleap-k8s-troubleshooting/blob/main/metaleap-k8s-troubleshooting.pdf) [[1]](https://tonylixu.medium.com/k8s-troubleshooting-hpa-unable-to-get-metrics-for-resource-b80899671d2f)<br>

[Visualizing Cgroups](https://miro.medium.com/v2/resize:fit:1400/format:webp/0*A6QdIrd-fC1M1Eeu) [[1]](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*VZEe-mdoRQADboTMcpSR6w.png)<br>
[Visualizing Cgroups in Kubernetes](https://miro.medium.com/v2/resize:fit:1400/format:webp/0*yO9CWHVsEL3Aze-X) [[1]](https://medium.com/geekculture/layer-by-layer-cgroup-in-kubernetes-c4e26bda676c) [[2]](https://man7.org/linux/man-pages/man7/cgroups.7.html) [[3]](https://kubernetes.io/docs/tasks/administer-cluster/kubeadm/configure-cgroup-driver/) [[4]](https://github.com/kubernetes/kubernetes/blob/cde45fb161c5a4bfa7cfe45dfd814f6cc95433f7/pkg/kubelet/cm/helpers_linux.go#L116)<br>

[Visualizing Kubernetes Benefits & Drawbacks](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F63a81651-7767-4161-bb47-5beb1e681315_1600x1230.png) [[1]](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Feb9b5087-426f-45cb-bb7a-a190323453f7_1230x1600.png) [[2]](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb56f56bd-fbd4-4ed1-9e69-b78bfe788c8a_1230x1600.png) [[3]](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F18ce810d-ce16-438a-83da-6b52d8d7c619_1230x1600.png)<br>

[Visualizing Kubernetes Architecture](https://airplane.ghost.io/content/images/d7605fbe-f2fb-40f1-99f4-8a2eeeda4bc6_img.png) [[1]](https://d33wubrfki0l68.cloudfront.net/2475489eaf20163ec0f54ddc1d92aa8d4c87c96b/e7c81/images/docs/components-of-kubernetes.svg) [[2]](https://cheatsheetseries.owasp.org/assets/Kubernetes_Architecture.png) [[3]](https://www.aquasec.com/wp-content/uploads/2020/11/Kubernetes-101-Architecture-Diagram-1.jpg) [[4]](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*V-fwKtm8k1ca2MnsAjhZxg.png)<br>
[Visualizing Kubernetes](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*KFafWgwSW3m7LIogIO3Rbw.png) [[1]](https://medium.com/programming-kubernetes/building-stuff-with-the-kubernetes-api-1-cc50a3642)<br>

[Visualizing the Kubeconfig File](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*1_CPoxcOYR_Uynu8tkdwMQ.png) [[1]](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*swJsT8BDqO1THFSq7AhSBA.png) [[2]](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*bOU0KxmuyTRaKp08ykYxXg.png) [[3]](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*vdjG88Zjg-lbW_yQor5Azg.png) [[4]](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*xH5TUFpmWtEBCBYe7Mrz-g.png) [[5]](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*C8vHKBhyU4BjluoFY9cFnA.png) [[6]](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*aMkKPmkuontJqqQel3a75Q.png)<br>
  
[Visualizing Pods and Nodes](https://kubernetes.io/docs/tutorials/kubernetes-basics/public/images/module_03_pods.svg)<br>
[Visualizing How a Kubernetes Pod Gets an IP Address](https://ronaknathani.com/blog/2020/08/how-a-kubernetes-pod-gets-an-ip-address/kubelet-cri-cni-flowchart.png)<br>
[Visualizing Pod Security Admission (PSA) Controller](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*6gSvHd-VYzfa5SlFC-szNw.gif) [[1]](https://medium.com/@muthanagavamsi/kubernetes-pod-security-admission-psa-20664cb3074d)<br>

[Visualizing CRI](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*ocwsqqkP6SUv8e-egJquDg.png) [[1]](https://landscape.cncf.io/guide#runtime--container-runtime)<br>
[Visualizing Architecture of The CRI Plugin](https://github.com/containerd/cri/blob/v1.11.1/docs/architecture.png) [[1]](https://github.com/containerd/cri/blob/v1.11.1/docs/architecture.md)<br>

[Visualizing CNI Plugin Popularity](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*xwdMl2qi-KthYx73sF3wfQ.png)<br>
[Visualizing the interactions between Containerd CRI Plugin and CNI plugins](https://ronaknathani.com/blog/2020/08/how-a-kubernetes-pod-gets-an-ip-address/kubelet-cri-cni-interactions.png
) [[1]](https://github.com/containerd/cri/blob/v1.11.1/docs/architecture.md)<br>
[Visualizing Bridge Networking](https://ronaknathani.com/blog/2020/08/how-a-kubernetes-pod-gets-an-ip-address/bridge-networking.png)<br>
[Visualizing Flannel Networking](https://ronaknathani.com/blog/2020/08/how-a-kubernetes-pod-gets-an-ip-address/flannel-networking.png)<br>
[Visualizing Native CNI Pod Networking](https://blogs.oracle.com/content/published/api/v1.1/assets/CONT78BF0A5D337F41A887531F7969A18FDE/Medium?cb=_cache_6177&format=jpg&channelToken=f7814d202b7d468686f50574164024ec)<br>
[Visualizing Flannel Overlay Networking](https://blogs.oracle.com/content/published/api/v1.1/assets/CONT94FDF8973EA4486AB65E88CA4DF72114/Medium?cb=_cache_6177&format=jpg&channelToken=f7814d202b7d468686f50574164024ec)<br>

[Visualizing the service access relationship in Kubernetes and service mesh (one sidecar per pod model)](https://cdn.thenewstack.io/media/2021/03/200a2844-image4.png)<br>

[Visualizing CSI Volume Plugin](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*RuYBVRJGfu1M0SC81Auzog.png)<br>
[Visualizing Kubernetes without CSI Volume Plugin](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*RuYBVRJGfu1M0SC81Auzog.png)<br>
[Visualizing Kubernetes nfs-client-provisioner](https://miro.medium.com/v2/resize:fit:2000/format:webp/1*OiN2woM7VjC437dYk5yeIg.jpeg) [[1]](https://medium.com/@gurpreet.singh_89/deploying-nfs-client-provisioner-in-kubernetes-75e240c6ec13)<br>

[Visualizing Kubernetes API](https://iximiuz.com/kubernetes-operator-pattern/kube-api-structure-3000-opt.png) [[1]](https://kubernetes.io/docs/concepts/overview/kubernetes-api/) [[2]](https://kubernetes.io/docs/concepts/overview/kubernetes-api/#api-groups-and-versioning) [[3]](https://github.com/kubernetes/community/blob/master/contributors/devel/sig-architecture/api-conventions.md)<br>
&ensp;&ensp;API objects are fully qualified by their<br>
&ensp;&ensp;API group, resource type, namespace (unless cluster-scoped), and name.<br>
    
[Visualizing Kubernetes Resources](https://laurinevala.medium.com/visualizing-kubernetes-resources-ee9d8c16d264) [[1]](https://miro.medium.com/v2/resize:fit:1400/format:webp/0*mdClEni7Za7F1DY5.png) [[2]](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*MK7WOMTF-Ks1sD67PIiphg.png)<br>
&ensp;&ensp;**IMPORTANT WARNING:**<br>
&ensp;&ensp;&ensp;&ensp;The word **resource** sometimes is used in the meaning of an object (but not vice versa)<br>
&ensp;&ensp;&ensp;&ensp;and sometimes in the meaning of an API endpoint - **context matters**!!!<br>
&ensp;&ensp;A resource specifies a Kubernetes API endpoint.<br>
&ensp;&ensp;The Kubernetes API consists of endpoints called resources.<br>
&ensp;&ensp;A Kubernetes Resource is a declarative API with a well defined Schema structure and endpoints.<br>
&ensp;&ensp;Because the structure of the Schema and Endpoints are predictable and structured,<br>
&ensp;&ensp;most Kubernetes tools work with any Kubernetes API<br>
&ensp;&ensp;even if they are not part of the core (e.g. [extensions through CRDs](https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.28/#customresourcedefinition-v1-apiextensions-k8s-io)).<br>
&ensp;&ensp;A Kubernetes resource is an endpoint/resource in the Kubernetes API that stores a collection of API objects of a certain kind;<br>
&ensp;&ensp;for example, the built-in pods resource contains a collection of Pod objects.<br>
&ensp;&ensp;A Kubernetes Resource Schema is the contents/structure of a yaml file.<br>

**Summary of Objects, Controllers, Operators and CRDs**<br>
&ensp;&ensp;**IMPORTANT WARNING:**<br>
&ensp;&ensp;&ensp;&ensp;The word **resource** sometimes is used in the meaning of an object (but not vice versa)<br>
&ensp;&ensp;&ensp;&ensp;and sometimes in the meaning of an API endpoint - **context matters**!!!<br>
&ensp;&ensp;A resource specifies a certain kind of Kubernetes object.<br>
&ensp;&ensp;Objects are like data structures.<br>
&ensp;&ensp;Controllers are like algorithms.<br>
&ensp;&ensp;Controllers are infinite loops that watch the actual and the desired states of your cluster.<br>
&ensp;&ensp;Controllers keep the current state of Kubernetes objects in sync with your declared desired state.<br>
&ensp;&ensp;When Objects & Controller states diverge,<br>
&ensp;&ensp;controllers start making changes aiming to bring the<br>
&ensp;&ensp;current state of the cluster closer to the desired one.<br>
&ensp;&ensp;All interactions with Kubernetes objects, directly or indirectly, happen through [Kubernetes API](https://kubernetes.io/docs/concepts/overview/kubernetes-api/) [[1]](https://github.com/kubernetes/community/blob/master/contributors/devel/sig-architecture/api-conventions.md).<br>
&ensp;&ensp;&ensp;&ensp;Directly via [Client Libraries](https://kubernetes.io/docs/reference/using-api/client-libraries/)<br>
&ensp;&ensp;&ensp;&ensp;Indirectly via [Command line tool (kubectl)](https://kubernetes.io/docs/reference/kubectl/)<br>
&ensp;&ensp;&ensp;&ensp;API objects are fully qualified by their<br>
&ensp;&ensp;&ensp;&ensp;API group, resource type, namespace (unless cluster-scoped), and name.<br>
&ensp;&ensp;[Operators](https://kubernetes.io/docs/concepts/extend-kubernetes/operator/) are how Kubernetes runs CRDs.<br>
&ensp;&ensp;A Kuberntes operator is a client of the Kubernetes API that acts as a controller for a Custom Resource. [[1]](https://github.com/operator-framework/community-operators/blob/master/docs/best-practices.md#summary) [[2]](https://operatorhub.io/) [[3]](https://rm-rf.ca/posts/2020/when-not-to-write-kubernetes-operator/)<br>
&ensp;&ensp;Operator = CRD + Custom Controller + your knowledge (aka., [SME](https://en.wikipedia.org/wiki/Subject-matter_expert)/domain/application specific knowledge)<br>
&ensp;&ensp;[CRDs](https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.28/#customresourcedefinition-v1-apiextensions-k8s-io) are a way to write your own custom Kubernetes object type [[1]](https://kubernetes.io/docs/tasks/extend-kubernetes/custom-resources/custom-resource-definitions/) [[2]](https://kubernetespodcast.com/episode/073-crds-extensibility-api-machinery/).<br>
&ensp;&ensp;When you create a new CustomResourceDefinition (CRD), the Kubernetes API Server<br>
&ensp;&ensp;creates a new RESTful resource path for each version you specify.<br>
&ensp;&ensp;A [Custom Resource](https://kubernetes.io/docs/concepts/extend-kubernetes/api-extension/custom-resources/#custom-resources) is is an extension of the Kubernetes API that is not necessarily available in a default Kubernetes installation.<br>
&ensp;&ensp;Custom resources let you store and retrieve structured data.<br>
&ensp;&ensp;A [Custom Controller](https://kubernetes.io/docs/concepts/extend-kubernetes/api-extension/custom-resources/#custom-controllers) is one of the ways in which you can extend Kubernetes.<br>
&ensp;&ensp;Custom controllers can handle in-built Kubernetes objects, such as Deployment, Service, in new ways.<br>
&ensp;&ensp;Custom controllers can work with any kind of resource, but they are especially effective when combined with custom resources.<br>
&ensp;&ensp;Custom resources are neat but useless in isolation.<br>
&ensp;&ensp;You need some custom code to interact with them (aka., a custom controller)<br>
&ensp;&ensp;When you combine a custom resource with a custom controller, custom resources provide a true declarative API.<br>

[Visualizing Kubernetes Objects & Interaction with System Resources](https://iximiuz.com/writing-kubernetes-controllers-operators/kdpv.png) [[1]](https://iximiuz.com/en/posts/kubernetes-operator-pattern/)<br>
[Visualizing the Kubernetes inlets-operator](https://iximiuz.com/kubernetes-operator-pattern/kube-operator-example-opt.gif) [[1]](https://github.com/inlets/inlets-operator) [[2]](https://github.com/inlets/inletsctl) [[3]](https://github.com/inlets/inlets-pro) [[4]](https://github.com/alexellis/arkade) [[5]](https://docs.inlets.dev/#/get-started/quickstart-ingresscontroller-cert-manager?id=expose-your-ingresscontroller-and-get-tls-from-letsencrypt)<br>
[Visualizing Kubernetes Go Client Controller: client-go](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*dmvNSeSIORAMaTF2WdE9fg.jpeg) [[1]](https://cloudark.medium.com/kubernetes-custom-controllers-b6c7d0668fdf) [[2]](https://github.com/kubernetes/sample-controller) [[3]](https://github.com/kubernetes/code-generator#readme)<br>
    
[Visualizing Kubernetes Services](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*jC28wQvePsmbic8AIqo_AA.png)<br>
[Visualizing Ingress vs. GatewayAPI](https://www.haproxy.com/assets/posts/kubernetes-ingress-vs-gateway-api.png)<br>
[Visualizing Gateway API](https://www.haproxy.com/assets/posts/kubernetes-gateway-api.png)<br>
[Visualizing GatewayAPI Multi-cluster](https://miro.medium.com/v2/resize:fit:828/format:webp/1*4cmidUu2s1NHSvTTSPs_Zg.png)<br>
[Visualizing Kubernetes Ingress Vs Gateway API](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*ZoMqn6ppkzNGLRWPDCWPXA.png)<br>
[Visualizing Kubernetes Ingress Routing](https://miro.medium.com/v2/resize:fit:1100/format:webp/1*sVPaw5BfTB2nh9lVEOSOsg.png)<br>
[Visualizing ClusterIP](https://kodekloud.com/blog/content/images/2023/02/ClusterIP-Service.png)<br>
[Visualizing a ClusterIP service](https://assets-global.website-files.com/64196dbe03e13c204de1b1c8/64774e3c68ce95e4149e38f0_58-image-2.png)<br>
[Visualizing NodePort](https://kodekloud.com/blog/content/images/2023/02/NodePort-Service.png)<br>
[Visualizing LoadBalancer Service](https://kodekloud.com/blog/content/images/2023/02/LoadBalancer-Service.png)<br>
[Visualizing a LoadBalancer Service](https://assets-global.website-files.com/64196dbe03e13c204de1b1c8/64774e59b2fabaa1dc069fcc_58-image-3.png)<br>
[Visualizing Service Ports](https://assets-global.website-files.com/64196dbe03e13c204de1b1c8/64774dfe998bc59f64a72793_58-image-1.png)<br>

[Visualizing Kubernetes Admission Controller](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*ysfawao2_9xTZYsWr_HztQ.png) [[1]](https://eminalemdar.medium.com/policy-management-in-kubernetes-is-changing-9d4808f548a0)<br>

[Visualizing Ingress Path](https://lh5.googleusercontent.com/ZKJZ5_b2BuaU9KnDYkeCOc0ePvpHQdhfMwvZPjU3pTK5aHL1022YNwY0G9qr4udwae7yI9hgGmhK3g0fuC66HK8ol3BtdVQ_z27nJFfHAfW38oMmhL9Ot8nc3r2Jxel5yTM9h5az33ws0DLwoCKmIZs)<br>

[Visualizing Virtual Kubelet](https://raw.githubusercontent.com/virtual-kubelet/virtual-kubelet/ce8a0ee8bd68f9c4c46a60a3db5e8e6e6c247839/website/static/img/diagram.svg) [[1]](https://github.com/virtual-kubelet/virtual-kubelet/blob/master/website/static/img/diagram.svg)<br>

[Visualizing how Kubelet, CRI, CRI-O, OCI & runc & kata-runtime fit together](https://miro.medium.com/v2/resize:fit:1100/format:webp/0*h2j060L-iJMlyW9F.jpg)<br>
  
[Visualizing how Podman, Containerd use crun, runc, gVisor, Nabla, katacontainers, Firecracker](https://adriancitu.files.wordpress.com/2021/12/untitled-diagram-image-run.drawio1.png)<br>

[Visualizing how Docker, Kubernetes, CRI, CRI-O, containerd, OCI & runc fit together](https://www.tutorialworks.com/assets/images/container-ecosystem.drawio.png?ezimgfmt=rs:704x1183/rscb6/ng:webp/ngcb6) [[1]](https://www.tutorialworks.com/difference-docker-containerd-runc-crio-oci/)<br>
[Visualizing how Kubernetes, CRI, CRI-O, containerd fit together](https://www.tutorialworks.com/assets/images/container-ecosystem-cri.drawio.png?ezimgfmt=rs:704x353/rscb6/ng:webp/ngcb6) [[1]](https://www.tutorialworks.com/difference-docker-containerd-runc-crio-oci/)<br>
[Visualizing how Kubelet, CRI, CRI-O, OCI & runc & kata-runtime fit together](https://miro.medium.com/v2/resize:fit:1100/format:webp/0*h2j060L-iJMlyW9F.jpg) [[1]](https://medium.com/kata-containers/why-kata-containers-doesnt-replace-kubernetes-75e484679727)<br>
[Visualizing of how Kubelet, CRI, Dockershim & CRI-Containerd & containerd fit together](https://lh6.googleusercontent.com/DUu4PrZ_KYIEEkTJ3s_T7o7X2BhT09ZuTAKvHFfbnD7F_gHb-6Hol0trGcEiU7Xu797SdkbFpDDUUDeB5XHTKFo9yab11kPjBWsg2PiPreu90Ktbak__isL9NkI-b_Ovh6GeLfrA)<br>
[Visualizing how Kubelet, containerd & runc fit together](https://lh3.googleusercontent.com/4RJz6Kbqa3z2AQ5QZQgNZKKLqa-VcSJq84IIEhhO6Rl0fIR09Aq8ODIiS2YgbuWbaCUP2kaZhC8EUPHJFrVRRXaLl09z0tVtjpcOTU_pdB17APS-qgbN_Ab5R9NNHX5ew8104-_X)<br>
[Visualizing CRI-Containerd Architecture: Kubelet -> gRPC -> cri-containerd -> gRPC -> containerd -> containerd shim](https://lh3.googleusercontent.com/U2WuYpgyAOknVzhwJbZz1y4Jk1wAlJDP1n42tiF-CpTEbvScGts_Z6_NOeVDF0SiaV4YRT1gl79MzdtD3mgzKET8xNDs6LAyjzH9J74xcs-0cgxBaPi6KbMsEhOH6WfqXu-H6Oq-) [[1]](https://cto.ai/blog/overview-of-different-container-runtimes/)<br>

[Visualizing 3-tier Architecture in Pools](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*LfqnGkJ5TGYDlMac4_WgdQ.png) [[1]](https://medium.com/@raphael.moutard/forget-your-microservices-the-unparalleled-benefits-of-pool-architecture-63b462989856)<br>

[Visualizing K8s Tools](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*dRZMWKGGvqS-No8sUYTH1g.png) [[1]](https://blog.devgenius.io/k8s-tools-kubeshark-464443bea7d7)<br>
[Visualizing K8s Tools Mind Map](https://github.com/metaleapca/metaleap-k8s-tools/blob/main/metaleap-k8s-tools.pdf)<br>
[Visualizing Kubeshark](https://miro.medium.com/v2/resize:fit:1400/format:webp/0*XTUlvLMNNtFURZQH.png)<br>
[Visualizing Service Map](https://miro.medium.com/v2/resize:fit:1400/format:webp/0*siUBtghrpU5niGkh.png)<br>

[Visualizing a Normal Deployment vs. a Helm Deployment](https://miro.medium.com/v2/resize:fit:1400/format:webp/0*hlqgMPyWMcfHU-GD) [[1]](https://amanpathakdevops.medium.com/day-26-kubernetes-helm-helm-charts-chapter-1-46e23aba25e6)<br>
    
[Visualizing Kube-State-Metrics (KSM)](https://miro.medium.com/v2/resize:fit:1400/format:webp/0*DmdAmgv_5nAn3l2G.png) [[1]](https://medium.com/@seifeddinerajhi/monitoring-kubernetes-clusters-with-kube-state-metrics-2b9e73a67895)<br>
[Visualizing Kube-State-Metrics (KSM) integration via go-client](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*BXJmqKBHikNTuA3l-K6ouw.png)<br>

[Visualizing Pulumi](https://www.pulumi.com/images/docs/reference/engine-block-diagram.png)<br>
[Visualizing Pulumi for Platform Teams](https://cdn.thenewstack.io/media/2023/10/fd3d0ac0-platform-teams-diagram-e1697458881245-1024x613.png)<br>

[Visualizing Amazon AWS Controllers for Kubernetes (ACK)](https://miro.medium.com/v2/resize:fit:1400/format:webp/0*cG9lUQ28fynCB_Li.png)<br>
[Visualizing AWS Transit Gateway](https://imgopt.infoq.com/fit-in/1200x2400/filters:quality(80)/filters:no_upscale()/news/2023/10/nomura-consul-service-discovery/en/resources/1Figure-2-service-flow-1696184017912.jpeg) [[1]](https://aws.amazon.com/transit-gateway/) [[2]](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/configuring-instance-metadata-service.html) [[3]](https://github.com/aws-samples/geographical-hierarchical-service-lookup-with-consul-on-aws)<br>

[Visualizing Redis Architectures](https://miro.medium.com/v2/resize:fit:1400/format:webp/0*Z8EXKcgNhmckzX4x.png)<br>
[Visualizing Redis Enterprise vs. Redis Open-Source]( https://miro.medium.com/v2/resize:fit:1400/0*gegAWGzw5szaUykG)<br>

[Visualizing a Kustomize Kubernetes Environment](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*2B6A0s-S3i2KLCbhY1IdeA.jpeg)<br>

[Visualizing the Flux Notification Controller](https://fluxcd.io/img/notification-controller.png)<br>
[Visualizing the Flux image-reflector-controller and image-automation-controller](https://fluxcd.io/img/image-update-automation.png)<br>

[Visualizing Flagger](https://raw.githubusercontent.com/fluxcd/flagger/main/docs/diagrams/flagger-overview.png)<br>

[Visualizing kopf](https://kopf.readthedocs.io/en/stable/_images/architecture-layers.png)<br>

[Visualizing Prometheus Architecture](https://github.com/prometheus/prometheus/raw/main/documentation/images/architecture.svg)<br>
[Visualizing Prometheus](https://miro.medium.com/v2/resize:fit:1400/format:webp/0*SYJgDDbJ34XMRy5j.png) [[1]](https://betterprogramming.pub/set-up-thanos-with-multi-tenancy-to-power-up-your-prometheus-70123e6ea555)<br>
[Visualizing Thanos for Prometheus](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*-DyHMDxAOFyL2r5-8DeHpA.png) [[1]](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*n_j1yPMvHL6gkDSGzq_LPw.png) [[2]](https://betterprogramming.pub/set-up-thanos-with-multi-tenancy-to-power-up-your-prometheus-70123e6ea555)<br>

[Visualizing SDLC](https://phoenixnap.com/blog/wp-content/uploads/2019/05/software-development-life-cycle.jpg) [[1]](https://camo.githubusercontent.com/6f0862439bd339eaa14f22a28af6fa77ed6d13a1f8072022d3f8f23df9638f86/68747470733a2f2f63646e2e6472696262626c652e636f6d2f7573657275706c6f61642f373732353831342f66696c652f6f726967696e616c2d61643334653561336435383761386139306236353836646536373731303232352e676966)<br>


### Additional Resources
[Kubetools - A Curated List of Kubernetes Tools](https://github.com/collabnix/kubetools)<br>
[Arcade](https://github.com/alexellis/arkade) - Open Source Marketplace For Developer Tools [[1]](https://github.com/inlets/inlets-operator/blob/fb1a2a0b951a710d1a54bcab4f1eef7d21ec0b91/chart/inlets-operator/crds/operator.inlets.dev_tunnels.yaml)<br>
[When Not to Write a Kubernetes Operator](https://rm-rf.ca/posts/2020/when-not-to-write-kubernetes-operator/)<br>
&ensp;&ensp;Operators should be reserved for more complex applications that require a<br>
&ensp;&ensp;noteworthy amount of manual intervention to keep running, upgrade or backup.<br>
&ensp;&ensp;This should be a relatively rare thing, Kube itself provides what most applications should need.<br>
&ensp;&ensp;Operators can be complex and add overhead to develop and maintain.<br>
&ensp;&ensp;You may reach that point someday but never assume it’s a requirement at the start.<br>

*) [Kubesploit:](https://medium.com/kubesploit/kubesploit-digest-january-2023-ec6253e2f0b3)<br>
&ensp;&ensp;The best Kubernetes, security-related articles, tutorials, libraries and tools republished

*) [CNCF:](https://www.cncf.io/) [Cloud Native Computing Foundation](https://en.wikipedia.org/wiki/Cloud_Native_Computing_Foundation)<br>
&ensp;&ensp;[CNCF Youtube Channel](https://www.youtube.com/c/cloudnativefdn/videos)<br>
&ensp;&ensp;[CNCF Cloud Native Interactive Landscape](https://landscape.cncf.io/)<br>

*) KubeCon:<br>
&ensp;&ensp;[KubeCon Europe](https://events.linuxfoundation.org/kubecon-cloudnativecon-europe/)<br>
&ensp;&ensp;[KubeCon North America](https://events.linuxfoundation.org/kubecon-cloudnativecon-north-america/)<br>

*) [Medium:](https://medium.com/) [[1]](https://www.facebook.com/medium) [[2]](https://twitter.com/medium) [[3]](https://www.instagram.com/medium)<br>
&ensp;&ensp;[Kubernetes on Medium](https://medium.com/tag/kubernetes)<br>
&ensp;&ensp;[How to Achieve Zero-Downtime Application with Kubernetes](https://blog.devops.dev/how-to-achieve-zero-downtime-application-with-kubernetes-ba52fdea9a9b)<br>
&ensp;&ensp;[Medium Youtube Channel](https://www.youtube.com/@medium/videos)<br>   
   
*) The New Stack:<br>
&ensp;&ensp;[The New Stack Youtube Channel](https://www.youtube.com/@TheNewStack/videos)<br>
&ensp;&ensp;[The New Stack Podcasts](https://thenewstack.io/podcasts/)<br>
&ensp;&ensp;https://thenewstack.io/category/cloud-native/<br>
&ensp;&ensp;https://thenewstack.io/platform-engineering/<br>
&ensp;&ensp;https://thenewstack.io/devops/<br>
&ensp;&ensp;https://thenewstack.io/ai/<br>
&ensp;&ensp;https://thenewstack.io/observability/<br>
&ensp;&ensp;https://thenewstack.io/serverless/<br>
&ensp;&ensp;https://thenewstack.io/webassembly/<br>
&ensp;&ensp;https://thenewstack.io/internal-developer-platform/<br>
&ensp;&ensp;[]()<br>
&ensp;&ensp;[]()<br>

*) [DevOps Toolkit:](https://www.youtube.com/@DevOpsToolkit/videos) [[1]](https://www.devopstoolkitseries.com/) [[2]](https://www.devopsparadox.com/) [[3]]()<br>
&ensp;&ensp;[Observability - Ask Me Anything With Ivan Merrill](https://www.youtube.com/watch?v=Hr_beKZDW_c)<br>
&ensp;&ensp;[Is eBPF The End Of Kubernetes Sidecar Containers?](https://www.youtube.com/watch?v=7ZVQSg9HX68)<br>
&ensp;&ensp;[Is CUE The Perfect Language For Kubernetes Manifests (Helm Templates Replacement)?](https://www.youtube.com/watch?v=m6g0aWggdUQ)<br>
&ensp;&ensp;[Is Timoni With CUE a Helm Replacement?](https://www.youtube.com/watch?v=bbE1BFCs548)<br>

*) [DevOpsTV:](https://techstrong.tv/) [[1]](https://techstronggroup.com/) [[2]](mailto:editor@devops.com)<br>
&ensp;&ensp;[DevOpsTV Youtube Channel](https://www.youtube.com/c/Devopsdotcom/videos)<br>
&ensp;&ensp;[]()<br>
&ensp;&ensp;[]()<br>

*) [StackState:](https://stackstate.com/)<br>
&ensp;&ensp;info@stackstate.com<br>
&ensp;&ensp;[StatckState Youtube Channel](https://www.youtube.com/@stackstate8010/videos)<br>
&ensp;&ensp;[]()<br>
&ensp;&ensp;[]()<br>

*) [Container Journal:](https://containerjournal.com/)<br>
&ensp;&ensp;[Container Journal Youtube  Playlists](https://www.youtube.com/playlist?list=PLotLY1RC8HovfOnTmbMQ0m609u9Eiq71N)<br>
&ensp;&ensp;[]()<br>

*) [Container Camp:](https://2020.container.camp/web)<br>
&ensp;&ensp;[Container Camp Youtube Channel](https://www.youtube.com/c/ContainerCamp/videos)<br>
&ensp;&ensp;[]()<br>  

*) [ContainerDays:]()<br>
&ensp;&ensp;[ContainerDays Youtube Channel](https://www.youtube.com/c/ContainerDays/videos)<br>
&ensp;&ensp;[]()<br>
   
*) [Continuous Delivery Foundation:](https://cd.foundation)<br>
&ensp;&ensp;[]()<br>


   
