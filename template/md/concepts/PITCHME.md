---
## Core Concepts
---
@title[Kubernetes Core Concepts]

@snap[north span-100]
@size[1.5em](Kubernetes Core Concepts)
@snapend

@snap[center span-100]
@ul
- what is kubernetes
- containers
- pods
- node
- scheduler
- replication controller
- service
@snapend

@snap[south template-note span-100]
(There is a lot more: deployments, daemonsets, statefulsets, crds...)
@snapend

---
@title[what is kubernetes]

@snap[north span-100]
@size[1.5em](What is kubernetes)
@snapend

@snap[center span-100]
Container orchestration, management, scheduling and service discovery.
<br><br>
@ul
- API driven application management
- Agents monitor endpoints for state changes (real-time)
- Controllers enforce desired state
- Labels identify resources (nodes, applications, services)
@snapend

---
@title[Kubernetes architecture]

@snap[center span-100]
![ARCHITECTURE](template/img/kube_architecture.png)
<br><br>
@snapend

@snap[south template-note span-100]
(source: https://www.aquasec.com/wiki/display/containers/Kubernetes+Architecture+101)
@snapend

---
@title[Containers]

@snap[north span-100]
@size[1.5em](Containers)
@snapend

@snap[center span-100]
A container is just an "isolated" process and **NOT** a lightweight Virtual Machine.
<br><br>

@snap[center span-100]
![CONTAINER](template/img/container.png)
@snapend

@snap[south span-100]
On *linux* kernel features (i.e. namespaces, cgroups) are used to implemented "containers"
@snapend


---
@title[Containers - continued]

@snap[north span-100]
@size[1.5em](Containers - cont)
@snapend

@snap[center span-100]
@ul
- application + dependencies = image
- Runtime environment
  - namespaces - what you can see (networks, mounts, UTC etc)
  - cgroups - what you can use (memory, cpu, i/o etc)
  - env vars
- Sharing host kernel makes containers very fast to provision and light on resources
@snapend

---
@title[Pods]

@snap[north span-100]
@size[1.5em](Pods)
@snapend

@snap[center span-100]
A unit of deployment and represents a running process in the cluster. It can also be thought of as a logical application. 
<br><br>

@snap[center span-100]
![CONTAINER](template/img/pod.png)
@snapend

---
@title[Pods - continued]

@snap[north span-100]
@size[1.5em](Pods - continued)
@snapend

@snap[center span-100]
@ul
- One or more containers
- Shared namespaces
  - networks+
  - storage
  - network IP address+
- metadata
- configuration
@snapend

@snap[south template-note span-100]
+Networking is provided by CNI and NOT Docker Networking
@snapend

---
@title[Node]

@snap[north span-100]
@size[1.5em](Node)
@snapend

@snap[center span-100]
Runs pods and proxies service requests
@ul
- managed by masters 
- container runtime (i.e. docker, rkt)
- kubelet
- kube-proxy
@snapend

---
@title[Scheduler]

@snap[north span-100]
@size[1.5em](Scheduler)
@snapend

@snap[center span-100]
Schedules pods to run on the nodes.
@ul
- Global scheduler
- Best fit chosen based on pod requirements 
- Pluggable
@snapend


