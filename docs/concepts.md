---
title: Concepts
permalink: /concepts/
---
This page provides some background on terms that are used throughout
the Metacontroller documentation.

## Kubernetes Concepts

These are some of the general [Kubernetes Concepts](https://kubernetes.io/docs/concepts/)
that are particularly relevant to Metacontroller.

### Controller

### Custom Controller

### Custom Resource

## Metacontroller Concepts

These are some concepts that are specific to Metacontroller.

### Metacontroller

### Lambda Controller

*Metacontroller* is a server that extends Kubernetes with APIs that encapsulate
the common parts of writing custom controllers.

When you create a controller with one of these APIs, you provide a function
that contains only the business logic specific to your controller.
Since these functions are called via webhooks, you can write them in any
language that can understand HTTP and JSON, and optionally host them with
a Functions-as-a-Service provider.

The Metacontroller server then executes a control loop on your behalf,
calling your function whenever necessary to decide what to do.

These callback-based custom controllers are called *Lambda Controllers*.
To keep the interface as simple as possible, each Lambda Controller API targets
a specific controller pattern, such as:

* CompositeController: *objects composed of other objects*
* DecoratorController: *attach new behavior to existing objects*

Support for other types of controller patterns will be added in the future.

### Lambda Hook