# learning-mesos-with-minimesos-workshop

## General Overview

### Workshop structure

* Presentation - Covers Mesos, Zookeeper, frameworks & Marathon
* Exercises using minimesos - Covers the same topics but now with focused exercises using minimesos
* Wrap up - Summarizes the topics and allows for Q&A

#### What is Mesos, what problem does it solve and what can I do with it?

Mesos is a distributed resource manager that allows you to treat your machines as a single computer. 

Benefits:

* Reuse the same machines for multiple workloads. Instead of sepaeate ES, Hadoop and Spark clusters use the same machines.
* Cost savings through increased utilization
* Mesos applications can react dynamically by spawning or removing tasks based on the environment

## Notes

* Add links to CS blogs in slides
* Downsides of Ansible / Chef is that they create a static partitioning of the cluster.
* Try satellite for monitoring 
* Add links to papers: Mesos, Zookeeper, PAXOS
* Try Apache Cotton

## Exercises

Running a web application on Mesos (node.js + mongo)
something like: https://github.com/ContainerSolutions/node-openshift-sample
2 containers: 1 for frontend (node js), 1 for backend (mongodb)

1. deploy frontend
2. deploy backend
3. link frontend and backend
4. scale up frontend
5. kill some of the frontend

### Mesos

* How can I find application logs?
* How can I see what is running on the cluster?
* How can I deploy a framework/application?
* How do I shut down a framework/application? (Note, cannot reconnect with same name after shutdown)
* How can I see how much resources the cluster has left?
* How do I authenticate a framework?
* How do I configure role reservations?
* What is the sandbox?
* How do I distribute files and binaries through the cluster?
* What is the difference between an application and a framework?
* Why would I want to write/use a framework?
* Where can I get state information? (state.json, tasks.json and /help)
* How do I meaure resource utilization of my Mesos cluster?
* What does it mean when I specify `cpus=1.5`?
* What is IP per container?
* What is a good level of utilization?
* What happens when you fork bomb a Mesos cluster?
* How can I monitor my cluster?
* What is the replicated log?
* How does DRF work?
* What happens if the master is killed?
* What is PAXOS?
* What is safe mode?
* What is checkpointing?
 
### Frameworks

* What is a framework?
* What is the difference between scheduler, executor and task?
* What is the lifecycle of a framework?
* How do I deploy ELK on Mesos?
* What is the sandbox?
* How does sandbox garbage collection work?
* What happens is a scheduler is killed?
* How do I write a framework?
** The easiest way is to use mesosframework. Second easiest way is to use Mesos Starter. Finally you can write your own using the HTTP or libmesos APIs in your favorite language.

### Zookeeper

* How can I check the contents of Zookeeper?
* What happens when a framework re-registers?
* How do I remove stale Zookeeper state?

### Service Discovery

* How do I deploy an application that requires a lookup of another service?

### Marathon

* How do I run a shell command on Marathon?
* How do I run a container on Marathon?
* How can I configure where my application gets deployed?
* How can I start applications using marathon when MM starts?
* How can I scale my simple application?
* How can I destroy?

### MiniMesos

* How do I configure resources in MM?
* How do I change the Mesos version in MM?
* How can I use MM with my integration tests?
* What is the Maven plugin?
