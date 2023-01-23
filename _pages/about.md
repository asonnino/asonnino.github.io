---
permalink: /
title: "About"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

I am a research scientist at [Mysten Labs](https://mystenlabs.com) working on the [Sui](https://sui.io) blockchain. I am also affiliated with the computer science department of [University College London (UCL)](https://www.ucl.ac.uk).

My research interests are in distributed systems, blockchains, and privacy enhancing technologies. These days I mostly work on Byzantine fault tolerant systems for blockchain applications including consensus protocols, consensus-less (broadcast-based) algorithms, and distributed execution engines.
I spend most of my time developing new algorithm to produce more performant distributed systems. A key aspect of my work is to leverage all the resources available to the machine and scale blockchain validators to run on multiple machines.

The typical goal of my projects is to go beyond the research stage, I spend considerable effort to implement and evaluate systems to ultimately run them in production. Feel free to drop me an email if you would like to work with me or get in touch.

<!-- <i class="fas fa-envelope"></i> alberto.sonnino@ucl.ac.uk<br>
<i class="fas fa-envelope"></i> alberto@mystenlabs.com -->

##  Short Bio

I received my PhD from [University College London (UCL)](https://www.ucl.ac.uk) advised by [George Danezis](http://www0.cs.ucl.ac.uk/staff/G.Danezis/) and [Jens Groth](http://www0.cs.ucl.ac.uk/staff/j.groth/). During my PhD I co-founded <kbd>chainspace.io</kbd>, which built a scalable and privacy-preserving smart contract platform. Chainspace scales by sharding its state among sub-quorums of nodes and supports privacy-preserving smart contracts by separating the contract's execution logic from its verification through zero-knowledge proofs. The company was built from several academic works such as [chainspace](/papers/chainspace.pdf), [byzcuit](/papers/byzcuit.pdf), and [coconut](/papers/coconut.pdf) (the first three chapters of my [PhD thesis](/papers/ucl-phd.pdf)). We were then acquired by Facebook (now named Meta) in February 2019.

I then helped design the [Novi wallet](https://www.facebook.com/help/1388094248345081/) and [Libra](https://www.diem.com/en-us/) payment system. Designing Libra (later renamed _Diem_) required numerous research innovations such as the [Jolteon](/papers/jolteon-and-ditto.pdf) consensus protocol, the [Carousel](/papers/carousel.pdf) leader election protocol, and the [Twins](/papers/twins.pdf) testing framework. The project also led to the creation of the open-source and production-ready [diem codebase](https://github.com/diem/diem) that became the foundation of [Aptos](https://aptoslabs.com).

While at Meta I also co-authored the [FastPay](/papers/fastpay.pdf) consensus-less payment system (the last chapter of my PhD thesis), the [Narwhal](/papers/narwhal-and-tusk.pdf) DAG-based mempool, and the [Bullshark](/papers/bullshark.pdf) consensus protocol. I then left Meta in 2022 to commercialize these projects, branded as [Sui](https://sui.io).

##  Selected Publications

{% assign bullshark = site.data.papers | where: "filename", "bullshark.pdf" | first %}
{% include paper.html paper=bullshark %}

{% assign narwhal_and_tusk = site.data.papers | where: "filename", "narwhal-and-tusk.pdf" | first %}
{% include paper.html paper=narwhal_and_tusk %}

{% assign fastpay = site.data.papers | where: "filename", "fastpay.pdf" | first %}
{% include paper.html paper=fastpay %}
