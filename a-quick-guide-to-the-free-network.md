---
title: 'Sean Tilley :: 一个通向自由网络的快速指南'
tags:
  - Fediverse
  - free internet
  - mastodon
date: 2020-12-03 21:25:25
---

[原文](https://medium.com/we-distribute/a-quick-guide-to-the-free-network-c069309f334)作者: [Sean Tilley](https://medium.com/@deadsuperhero?source=post*page-----c069309f334--------------------------------) 译者：晚霞

很多刚接触*联盟*网络的人可能会听到一个随意的说法，就是*fediverse*，可能会好奇这个词是什么意思。简单的解释可能是它是 "*federation*"和 "*universe*"的结合，但实际上它比这更复杂一些。让我们深入了解一下这只“野兽”的本质，以及一些历史。

目前，在*联盟的*社交通信领域有两个超级网络，它们运行在不同的协议上。它们分别被称为**The Fediverse**，和**The Federation**。虽然这两个超级网络的功能相似，甚至有相似的目的，但它们各自来源于不同的发展历史，并由此产生了不同的协议栈。这一系列重叠的网络在宏观上可以称为**自由网络**(**The Free Network**)。

![](https://freeformsuite.files.wordpress.com/2020/12/1ucqhwil3f0av0awmafmdrw.png?w=589)

8个不同的平台，每个平台都是相互独立开发的。Hubzilla和Friendica可以与这两个网络对话，因为这些项目是与协议无关(protocol-agnostic)的，可以通过插件进行扩展。

## 什么是*Fediverse*？

[The Fediverse](https://fediverse.kranglabs.com/)历来是作为一个微型Blog运行的，并使用*OStatus*协议让服务器之间相互沟通。它总共拉拢了六个不同的平台。*GNU Social*、*postActiv*、*Pleroma*、*Mastodon*、*Friendica*和*Hubzilla*。

*Fediverse*最初是由少数几台服务器成立的，这些服务器都运行在*StatusNet*平台上，可以简单地说是类似于*Twitter*，但不同的是它有一个特殊的群体交流功能。由于其微型Blog的特性，帖子和评论被认为是同一类型的对象(object)，称为*Status*。

*StatusNet*最终被转入[GNU Social](https://gnu.io/social/)项目中，并在该项目中继续稳步发展。它已经被分叉到[postActiv](https://www.postactiv.com/)项目中，该项目旨在清理系统的后台和用户界面。[Mastodon](https://joinmastodon.org/)最初是作为一个*Rails-based*的*Ruby*的*OStatus实现*而开发的，而且也可以连接到这这个网络。最后，[Pleroma](https://gitgud.io/lambadalambda/pleroma)项目最初是作为*GNU Social*的替代前端，但现在有了自己用*Elixir*编写的后端。

## 什么是*Federation*？

[The Federation](https://the-federation.info/)是一个由278个不同的连接着的服务器组成的*Interop*网络，这些服务器使用*Diaspora federation*协议进行通信。这是一个与*OStatus*不同的通信标准，允许四种不同的平台相互通信：*Diaspora*、*Friendica*、*Hubzilla*和*Socialhome*。

*Federation*最初是在2010年开始的，服务器只运行[Diaspora](https://diaspora.software/)。从结构上看，Diaspora的功能更像*Facebook*：它支持长篇内容而不是短篇，每个帖子都有一个指定的线程供评论。它还支持私密状态(private statuses)和一个收发direct messages的inbox。

2012年，[Friendica](http://friendi.ca/)项目破天荒地对*Diaspora*通信协议进行了逆向设计，并从头开始编写了一个PHP实现库，**让Friendica用户和Diaspora用户可以互相对话**。这项工作最终被移植到[Hubzilla](https://project.hubzilla.org/page/hubzilla/hubzilla-project)上，这是一个具有云存储(Cloud Storage)和id提供(identity provision)功能的内容管理系统。

2016年初，*Diaspora*项目的前志愿者贡献者[Jason Robinson](https://jasonrobinson.me/)发布了[Socialhome](https://socialhome.network/)。由于该平台利用的是*Django*而非*Rails*，Jason不得不从头开始编写[自己的federation-Python库](https://github.com/jaywink/federation)。目前，*Socialhome*在自己的发展史上还处于刚开始，最新的版本是0.4.0。

## 未来怎样?

目前，该领域的几个项目正在努力采用新的补充协议，目的是在彼此之间建立更好的桥梁。拟议的开发可能最终会是这样的：

![](https://freeformsuite.files.wordpress.com/2020/12/13pek-fwq7bnovcnxfvdnuq.png?w=603)

*Diaspora*目前还没有新协议的计划，只是对自己的协议进行了大幅升级。*postActiv*打算在未来的版本中采用对*Diaspora Federation*的支持。*Mastodon*刚刚发布了对*ActivityPub*的支持，*Pleroma*，*Socialhome*和*GNU Social*也在考虑采用。*Nextcloud*也明显进入了*Federation*领域，*Hubzilla*和*Friendica*可能都会作为扩展支持*ActivityPub*协议。

![](https://freeformsuite.files.wordpress.com/2020/12/1rea3ego1v1vc90e1t82uga.png?w=380)

随着时间的推移，这些截然不同的超级网络很可能会折叠成一个包含所有人的联合超级网络，最大限度地提高九个不同系统之间的互操作性，甚至可能更多。虽然这样的情景还很遥远，但我们完全有可能看到这个空间内所有的主要项目都最终能相互连接。