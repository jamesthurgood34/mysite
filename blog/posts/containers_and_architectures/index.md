---
date: "2024-10-06"
layout: post
title: Containers and Architectures
categories: [containers]
---

This is a short blog covering my recent experience in getting a containers hosted on a raspberry PI for a personal project.

# What Are Containers

To start with, containers are great! 


For those new to containers they allow you to build an environment and freeze it in a given state. They are built in layers, so you take a base image which contains various binaries e.g. the distribution of linux you wish to use. You can then add your project specific dependencies, and publish any new layers to a container registry. Others can then take your container and build on it in turn. These layers make containers incredibly space and time efficient. A registry (the place where you externally store your container) only need save each layer, so if you have 100 container all building off of the same base container you need only save the base once and just store the difference for each of the 100.

A common issue for engineers is the fact that you write code locally (e.g. a laptop) but you are likely not going to want to run that code on your laptop 24/7. Now ensues a problem many an engineer has faced at one time or another. Setting up a local development environment and ensuring the infrastructure you are deploying to is identical. If it is not then you are likely going to run into issues. 

# Archetectures