# 100 Days of Kubernetes
This repository holds a short description of what I have done and learned everyday while going through the 100 Days of Kubernetes challenge

* * * 

This book holds all my notes for every day. This is a work-in-progress repository which may be heavily altered in its structure depending on where I go. 

I am using multiple resources to structure my learning over the coming 100 days. For one, I keep track of what I have been doing in my public GitHub repository. This will only contain short notes on my progress every day to keep an overview over what I have been learning/doing every day. 

This book serves as a Wiki including longer notes of what I have been doing. This includes knowledge from different resources I use to get a better picture of the overall structure and use of Kubernetes. 

### Resources used
- 100daysofkubernetes.io
- Book: Kubernetes Up and Running
- Jeff Geerling's YouTube "Kubernetes 101" series
- ixmiuz Blog posts
- Kelsey Hightower's "Kubernetes The Hard Way"

* * *

## Day 1: 
In short words, Kubernetes can be defined as

```an open source orchestrator, which deploys containerized applications and provides the Software necessary for building and deploying **reliable**, and **scalable** distributed systems.```

Why would one need such a tool in the first place though? Modern infrastructures/products are usually split up and distributed in various services. This is commonly referred to as Microservice architecture[^1] [^2]. What this basically means that an application is as a collection of distributed services. The services are usually hosted in different places and have to communicate with each other over the network via APIs. There are various benefits of this over a [monolithic application](https://en.wikipedia.org/wiki/Monolithic_application#:~:text=In%20software%20engineering%2C%20a%20monolithic,independent%20from%20other%20computing%20applications.). 

For one if your application needs scaling, you don't have to scale the hardware with it. Also, different teams can work on different services and do not need to constantly communicate with each other, because they are only responsible for their specific service. This is very beneficial for a business, as it can focus on organizing the whole architecture around it's specific capabilities. 

All that being said, microservice architecture comes with it's own challenges. All the different services need to be coordinated with each other and be able to communicate with each other over the network, especially as they are hosted on distributed systems [^3]. 

This is precisely why Kubernetes is so helpful, as it directly helps with the main aspects of such an architecture: **reliability**, **availability** and **scalability**. They must be _reliable_ in the sense that they *cannot fail, even if a part of the system crashes or otherwise stops working* [^4]. They must be _available_ at all times, even during software updates and maintenance. And their capacity must quickly be able to be scaled based on the current need without affecting any of the previous two key characteristics. 

[^1]: For more in-depth information check the Wikipedia page: https://en.wikipedia.org/wiki/Microservices
[^2]: Or else this very helpful documentation: https://microservices.io/
[^3]: A "Distributed system" is eventually nothing other than an environment in which the different components are spread across multiple different computers. 
[^4]: Quoting "Kubernetes Up and Running" here. 
