---
title: ethtool
category: Command, Tool
date: 2019-09-16T12:00:00Z
lastmod: 2019-09-16T12:00:00Z
comment: true
adsense: true
---

NIC을 제어하는 ethtool 사용법을 정리한다.

***

* TOC
{:toc}

***

### 1. ethtool

#### 1.1. # ethtool [Interface]

{% highlight console %}
# ethtool eth0
Settings for eth0:
        Supported ports: [ ]
        Supported link modes:   Not reported
        Supported pause frame use: No
        Supports auto-negotiation: No
        Supported FEC modes: Not reported
        Advertised link modes:  Not reported
        Advertised pause frame use: No
        Advertised auto-negotiation: No
        Advertised FEC modes: Not reported
        Speed: 1000Mb/s
        Duplex: Full
        Port: Other
        PHYAD: 0
        Transceiver: internal
        Auto-negotiation: off
        Link detected: yes
{% endhighlight %}
<figure>
<figcaption class="caption">[Shell 1] ethtool eth0</figcaption>
</figure>

[Interface] NIC 정보를 출력한다. [Shell 1]은 ethtool을 이용하여 eth0 Interface 정보를 출력하는 Shell의 모습을 나타내고 있다. [Shell 1]에서 eth0의 Bandwidth(Speed)와 Duplex Mode를 확인할 수 있다.

#### 1.2. # ethtool [Interface] [speed 10|100|1000] [duplex half|full]

[Interface] NIC의 Bandwidth(Speed)와 Duplex Mode를 설정한다.