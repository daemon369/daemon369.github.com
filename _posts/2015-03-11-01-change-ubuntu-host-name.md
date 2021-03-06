---
layout: post
keywords: ubuntu, host name, linux
description: change ubuntu host name
title: "修改 Ubuntu 主机名"
categories: [Linux]
tags: [ubuntu, host name, linux]
group: Linux
icon: file-alt
date: 2015-03-11 00:00:00
---

在 Ubuntu 中修改主机名，需修改两个文件。

首先是 */etc/hostname* 文件：

    $ cat /etc/hostname
    myhostname

然后是 */etc/hosts* 文件：

<!--excerpt-->

    $ cat /etc/hosts
    127.0.0.1	localhost
    127.0.1.1	myhostname

    # The following lines are desirable for IPv6 capable hosts
    ::1     ip6-localhost ip6-loopback
    fe00::0 ip6-localnet
    ff00::0 ip6-mcastprefix
    ff02::1 ip6-allnodes
    ff02::2 ip6-allrouters

将上面两个文件中的旧的主机名 *myhostname* 修改为新的主机名，重启机器即可。
