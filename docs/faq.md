---
title: Frequently Asked Questions
classes: wide
permalink: /faq/
---
This page answers some common questions encountered while
evaluating, setting up, and using Metacontroller.

## Evaluating Metacontroller

### How does Metacontroller compare with other tools?

* 

See the [design docs](/design/) for more on why Metacontroller works the way it does.

### What is Metacontroller good for?

* configuration abstraction - separate app domain config from k8s domain config

### What is Metacontroller not good for?

* configuration management

alternatives:

* Propose a new controller pattern for Metacontroller.
* Use a tool tailored for your use case (CI/CD, workflow automation, etc.).
* 

### Do I have to use CRD?

### What does the name Metacontroller mean?

The name *Metacontroller* comes from the English words *meta* and *controller*.
Metacontroller is a *controller controller* --
a [controller](/concepts/#controller) that controls other controllers.

### How do you pronounce Metacontroller?

Please see the [pronunciation guide](/pronunciation/).

## Setting Up Metacontroller

### Do I need to be a cluster admin to install Metacontroller?

### Why is Metacontroller shared cluster-wide?

### Why does Metacontroller need these permissions?

### Does Metacontroller have to be in its own namespace?

### Can I install Metacontroller for only one namespace?

## Using Metacontroller

### Which languages can I write hooks in?

### How do I access the Kubernetes API from my hook?

### How do I host my hook?

### What are the best practices for designing controllers?

Please see the dedicated [best practices guide](/guide/best-practices/).

### How do I troubleshoot problems?

Please see the dedicated [troubleshooting guide](/guide/troubleshooting/).