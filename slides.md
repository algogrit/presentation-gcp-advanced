layout: true

.signature[@algogrit]

---

class: center, middle

# GCP Advanced

Gaurav Agarwal

---

# Agenda

- Cloud & Serverless is AWESOME!

---

class: center, middle

## Who is this class for?

---

- Application Developers

- SRE & devops engineers

---
class: center, middle

## What are we going to learn?

---
class: center, middle

*Outline*

---

class: center, middle

![Me](assets/images/me.png)

Software Engineer & Product Developer

Director of Engineering & Founder @ https://codermana.com

ex-Tarka Labs, ex-BrowserStack, ex-ThoughtWorks

---

class: center, middle

Co-organizer of Chennai Go meetup

Volunteer at Golang India - Remote study group

---

class: center, middle

*What we wanted*

![In-class Training](assets/images/professional-training-courses.jpg)

---

class: center, middle

*What we got*

![WFH](assets/images/wfh.jpg)

---

## As a instructor

- I promise to

  - make this class as interactive as possible

  - use as many resources as available to keep you engaged

  - ensure everyone's questions are addressed

---

## What I need from you

- Be vocal

  - Let me know if there any audio/video issues ASAP

  - Feel free to interrupt me and ask me questions

- Be punctual

- Give feedback

- Work on the exercises

- Be *on mute* unless you are speaking

---
class: center, middle

## Class Progression

---
class: center, middle

![Class progression](assets/images/learning-curve.jpg)

---
class: center, middle

Here you are trying to *learn* something, while here your *brain* is doing you a favor by making sure the learning doesn't stick!

---

### Some tips

- Slow down => stop & think
  - listen for the questions and answer

- Do the exercises
  - not add-ons; not optional

- There are no dumb questions!

- Drink water. Lots of it!

---

### Some tips (continued)

- Take notes
  - Try: *Repetitive Spaced Out Learning*

- Talk about it out loud

- Listen to your brain

- *Experiment!*

---
class: center, middle

### 📚 Content ` > ` 🕒 Time

---
class: center, middle

## Show of hands

*Yay's - in Chat*

---
class: center, middle

## Application Development Process

---
class: center, middle

### Monolithic architecture

---
class: center, middle

A monolithic application is built as a single unit.

---

Typical enterprise applications are built in three parts:

- A database — consisting of many tables usually in a relational database management system

- A client-side user interface — consisting of HTML pages and/or JavaScript running in a browser)

- A server-side application — which will handle HTTP requests, execute domain-specific logic, retrieve and update data from the database, and populate the HTML views to be sent to the browser.

---
class: center, middle

*single logical executable*

![Monolith Logic](assets/images/monolith-logic.jpg)

---
class: center, middle

Monolith apps allow you to set your deployment once and then simply adjust it based on ongoing changes.

---

#### Benefits of Monolith

- Simple to develop — At the beginning of a project it is much easier to go with Monolithic Architecture.

- Simple to test. For example, you can implement end-to-end testing by simply launching the application and testing the UI with Selenium.

- Simple to deploy. You have to copy the packaged application to a server.

- Simple to scale horizontally by running multiple copies behind a load balancer.

---
class: center, middle

![Monolith eCom](assets/images/monolith-ecom.jpg)

---
class: center, middle

*Makes it simple to deploy*

---

#### Drawbacks of Monolith

- Tight coupling between components

- Maintenance — If Application is too large and complex to understand entirely, it is challenging to make changes fast and correctly.

- The size of the application can slow down the start-up time.

- You must redeploy the entire application on each update.

- Monolithic applications can also be challenging to scale when different modules have conflicting resource requirements.

- Reliability — Bug in any module (e.g. memory leak) can potentially bring down the entire process. Moreover, since all instances of the application are identical, that bug impact the availability of the entire application

- Regardless of how easy the initial stages may seem, Monolithic applications have difficulty to adopting new and advance technologies.

---
class: center, middle

Since changes in languages or frameworks affect an entire application, it requires efforts to thoroughly work with the app details, hence it is costly considering both time and efforts.

---
class: center, middle

*Harder to build and maintain parts of application by multiple teams*

---
class: center, middle

### Building an application in a microservice architecture

---
class: center, middle

*Microservices are better suited to scalability*

---
class: center, middle

![Monolith vs Microservice](assets/images/monolith-vs-microservice.jpg)

---

#### Benefits of Microservices

- Enables the continuous delivery and deployment of large, complex applications.

- Better testability — services are smaller and faster to test.

- Better deployability — services can be deployed independently.

- It enables you to organize the development effort around multiple teams. Each team is responsible for one or more single service. Each team can develop, deploy and scale their services independently of all of the other teams.

- Each microservice is relatively small

.content-credits[https://medium.com/koderlabs/introduction-to-monolithic-architecture-and-microservices-architecture-b211a5955c63]

---

- Comfortable for a developer to understand

- The IDE is faster making developers more productive

- The application starts faster, which makes developers more productive, and speeds up deployments

- Improved fault isolation. For example, if there is a memory leak in one service then only that service is affected. The other services continue to handle requests. In comparison, one misbehaving component of a monolithic architecture can bring down the entire system.

- Eliminates any long-term commitment to a technology stack. When developing a new service you can pick a new technology stack. Similarly, when making major changes to an existing service you can rewrite it using a new technology stack.

.content-credits[https://medium.com/koderlabs/introduction-to-monolithic-architecture-and-microservices-architecture-b211a5955c63]

---
class: center, middle

#### Modes of communication

![modes-of-communication](assets/images/microservice-modes-of-communication.png)

---
class: center, middle

Let's decompose the monolith Ecomm application into microservices...

---
class: center, middle

![ecomm microservice](assets/images/ecom-microservice.png)

---
class: center, middle

*But...*

---

- How do I manage the dependencies?

- How do I deploy it?

- How do I manage the configuration?

- How do I manage scaling/monitoring/logging?

- Service discovery?

---
class: center, middle

#### Dependency Hell - [Problem](https://github.com/AgarwalConsulting/DockerTraining/blob/master/Problem.md)

---
class: center, middle

![Dependency Hell](assets/images/dependency-hell.jpg)

.image-credits[https://blog.newrelic.com/technology/app-centric-docker-monitoring-webinar/attachment/dependency-hell/]

---
class: center, middle

##### Solutions?

---
class: center, middle

Let's start with VM?

---
class: center, middle

*Virtual Machines* aka Hardware Virtualization

---
class: center, middle

![VM Architecture](assets/images/virtual-server-architecture.jpg)

.image-credits[https://www.nakivo.com/blog/physical-servers-vs-virtual-machines-key-differences-similarities/]

---
class: center, middle

![Physical vs Virtual](assets/images/physical-vs-vm.png)

---
class: center, middle

*Leads to resource wastage*

---
class: center, middle

How about Docker?

---
class: center, middle

## Docker

---
class: center, middle

### VM vs Containers

![VM vs Container](assets/images/vms-vs-containers.jpg)

.image-credits[https://www.weave.works/blog/a-practical-guide-to-choosing-between-docker-containers-and-vms]

---
class: center, middle

### Hypervisor vs Containers

![Hypervisor vs Container](assets/images/hypervisors-vs-containers.png)

.image-credits[https://www.docker.com/blog/containers-replacing-virtual-machines/]

---
class: center, middle

### Docker: under the hood

---
class: center, middle

![Docker Under](assets/images/docker-under.png)

---

class: center, middle

[OCI Runtime Specification](https://github.com/opencontainers/runtime-spec)

The Open Container Initiative develops specifications for standards on Operating System process and application containers.

.content-credits[https://github.com/opencontainers/runtime-spec/blob/master/spec.md]

---
class: center, middle

`docker run hello-world`

---

### Primer

![Architecture](assets/images/architecture.svg)

.image-credits[https://docs.docker.com/engine/docker-overview/]

---
class: center, middle

### Containers

---
class: center, middle

![Container Analogy](assets/images/container-analogy.png)

---

- Using `docker run`, to start a container

- Using `docker ps`, to view status of containers

- Using `docker stop`, to stop a container

- Using `docker rm`, to remove a stopped container

---
class: center, middle

*Exercise*: Run a linux container, create a file inside it and stop it

---
class: center, middle

Containers are *ephemeral*

---
class: center, middle

### Images

---

#### Key concepts

- Image is the definition of what a **container** is created from.

- Images are **immutable**. If you make changes, a new image must be built.

- Images are made of **layers**.

- Images are **inherited** from **base images** and can be many levels deep.

- `docker images`

.content-credits[https://www.vergeops.com/]

---
class: center, middle

#### Dockerfile

Or `dockerfile`, `my-dockerfile`, ...

---

- Use `Dockerfile`

  - *Infrastructure as Code*

  - All images are based on other images as their parent.

  - You must choose a parent, or `FROM` image.

  - `scratch` is the base empty image supplied by Docker.

  - Base images include all settings, files, what command runs at startup, etc.

- Create an image using

  - `docker build`

---

Here is the format of the `Dockerfile`:

```Dockerfile
# Comment
INSTRUCTION arguments
```

---

Eg. [`hello-world`'s `Dockerfile`](https://hub.docker.com/_/hello-world)

```bash
cat Dockerfile
```

```dockerfile
FROM scratch
COPY hello /
CMD ["/hello"]
```

---

#### Other Commands

There are just a handful of simple `Instructions`:

```bash
FROM # which image this inherits from
LABEL # custom information
WORKDIR # Change to a directory until changed again.
  # Works like cd
USER # Change to a user
RUN # Run a Linux command in a new layer.
  # The command is dependent on which shell is in the image.
EXPOSE # Tells what ports this container will listen on.
  # Does not actually publish a port, but is rather like documentation.
ADD # copy files into the container
COPY # copy files into the container.
  # Similar to ADD
ENTRYPOINT # The command to be run when container is started.
  # This is inherited from a base image.
CMD # provides defaults to be run after the ENTRYPOINT.
  # Also inherited from the base image.
```

[More...](https://docs.docker.com/engine/reference/builder/)

---

#### Layers

- Images are made of **layers**.

- Each instruction in a `Dockerfile` adds a layer. (*True* for older Docker installations)

- When pushing/pulling an image to a repository (more to come), only the **changed layers** are pushed to save bandwidth.

- When building an image, Docker steps through the instructions in your Dockerfile, executing each in the order specified.

---
class: center, middle

Only the instructions *RUN, COPY, ADD* create layers.

.content-credits[https://docs.docker.com/develop/develop-images/dockerfile_best-practices/]

---
class: center, middle

![Image Layers](assets/images/layers-example.png)

.image-credits[https://www.vergeops.com/]

---

#### Image Tags

- You can uniquely identify an image using a tag name

- `docker build -t <image-name>:<tag-name> .`

- `latest` is the default tag name

---
class: center, middle

*Optional Exercise*: Create a `hello-world` image, similar to [`hello-haskell`](https://github.com/AgarwalConsulting/DockerTraining/tree/master/examples/0-hello-world/hello-haskell)

---
class: center, middle

![Dockerfile vs Image vs Container](assets/images/docker-process.png)

.image-credits[https://ekababisong.org/docker-kubeflow-for-poets/]

---
class: center, middle

### Registry

---

- Many options: Docker Hub, AWS ECR, GCP Container Registry, ...

- Default: https://hub.docker.com/

- Private repository...

---

#### Pulling from a repository

`docker pull hello-world`

---

#### Pushing to a repository

`docker push <image-name>:<tag-name>`

---
class: center, middle

*Optional Exercise*: [Push the `hello-world` image to hub](https://github.com/AgarwalConsulting/DockerTraining/blob/master/challenges/pushing-to-remote-repo.md), ask a participant to run it on their system

---
class: center, middle

Let's look at the `Dockerfile` of the ecommerce microservice...

---

Docker can also manage:

- Network between containers

- Volumes and storage for containers

- Life of the container: `restart_policy`

---
class: center, middle

#### [12 Factor](https://12-factor-apps.slides.algogrit.com/) Apps

---
class: center, middle

### Orchestrating your containers (Managing multiple containers)

---
class: center, middle

#### Docker Compose

---
class: center, middle

How about scaling it to multiple machines...

---
class: center, middle

### Thought Experiment: [Search Engine](https://github.com/AgarwalConsulting/Kubernetes-Training/blob/master/Problem.md)

---

- cluster of machines
- From ~10 to millions of microservices
- Manage/Share resources efficiently
  - Memory
  - CPU
  - Storage
  - GPU
  - ...
- Fault Tolerance
  - Healing & resiliency
- Isolation
- Networking
  - Service Discovery
- Managing Deployment
- Auto-Scaling
- ...

---
class: center, middle

## Kubernetes

---
class: center, middle

### Kubernetes Architecture

![Components](assets/images/components-of-kubernetes.png)

---
class: center, middle

### Control Plane Components

Control plane components can be run on any machine in the cluster. However, for simplicity, set up scripts typically start all control plane components on the same machine, and do not run user containers on this machine.

---
class: center, middle

### Worker Plane components - Nodes

Node components run on every node, maintaining running pods and providing the Kubernetes runtime environment.

---
class: center, middle

### K8s - CLI Tools

---

#### `kubeadm`

- The `kubeadm` tool helps you [bootstrap](https://kubernetes.io/docs/reference/setup-tools/kubeadm/kubeadm/) a minimum viable Kubernetes cluster that conforms to best practices.

  *In fact, you can use `kubeadm` to set up a cluster that will pass the [Kubernetes Conformance tests](https://kubernetes.io/blog/2017/10/software-conformance-certification/).*

- A simple way for you to try out Kubernetes, possibly for the first time.

- A way for existing users to automate setting up a cluster and test their application.

- A building block in other ecosystem and/or installer tools with a larger scope.

.content-credits[https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/create-cluster-kubeadm/]

---

#### `kubectl`

- The `kubectl` command line tool lets you control Kubernetes clusters.

- For configuration, kubectl looks for a file named `config` in the `$HOME/.kube` directory.

- You can specify other kubeconfig files by setting the `KUBECONFIG` environment variable or by setting the `--kubeconfig` flag.

- Makes it reasonably easy to work with multiple clusters using: `kubectl config` & `contexts`

.content-credits[https://kubernetes.io/docs/reference/kubectl/overview/]

---

#### [`kind`](https://kind.sigs.k8s.io/docs/user/quick-start/)

- command line tool which allows for simulating a multi node k8s cluster

---
class: center, middle

### K8s Basics (Cluster Computing)

---



---
class: center, middle

Code
https://github.com/AgarwalConsulting/GCP-Training

Slides
https://gcp-advanced.slides.algogrit.com
