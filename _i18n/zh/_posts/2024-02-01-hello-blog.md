---
layout: distill
title: 你好，SLAM2.0.
date: 2024-02-01 00:00:00
description: '在2016年，发表于TRO的论文《Past, Present, and Future of Simultaneous Localization and Mapping: Toward the Robust-Perception Age》中，回顾了SLAM（同时定位与建图）领域的一个经典问题：“SLAM问题是否已经得到解决？”时至今日，距离这一讨论已经过去了八年。随着SLAM2.0概念的提出，我们在2024年重新回顾这个问题，并将围绕以下两个核心问题展开讨论：1. 什么是SLAM？2.我们将如何理解SLAM2.0？'
authors:
  - name: 吴奇 
    affiliations: 
      name: SJTU
bibliography: blogs.bib
tags: VIO,SLAM
categories: Discussion
featured: false
comments: true
---

# 写作思路

什么是SLAM->为什么SLAM受欢迎？SLAM有哪些部分组成？->目前有哪些流行的框架->如何评价一个系统的好坏？->SLAM是否完结？->该如何定义SLAM2.0?

# 前言

SLAM包括对配备有板载传感器的机器人状态进行同时估计，以及构建传感器感知到的环境模型（地图）。不依赖GNSS信号强度，SLAM可以在任何场景下实现无人设备的自主定位和场景描述。所以SLAM的流行也部分得益于移动机器人室内应用的出现。

The genesis of the probabilistic SLAM problem occurred at the 1986 IEEE Robotics and Automation Conference held in San Francisco. This was a time when probabilistic methods were only just beginning to be introduced into both robotics and AI.

SLAM这个概念最早是由谁提出的？

即时定位与建图算法（后面都简称SLAM）最早是在1986年的IEEE Robotics and Automation Conference大会上提出。当时的研究者渴望将概率方法引入到机器人和AI领域，他们希望移动机器人能通过板载传感器实现在未知环境下的定位与环境描述。这场讨论中的参与者中，有很多后面引领多年SLAM潮流的大佬们，如Hugh Durrant-Whyte，Peter Cheeseman，Jim Crowley，Raja Chatila, Oliver Faugeras Randal Smith等。像很多传说一样， 当时他们讨论激烈，许多纸巾和餐巾纸上都记录着关于一致地图绘制的长时间讨论。

换个思路：1986年讨论->这些学者在一块讨论，产生了SLAM这个领域。

# SLAM 1.0

