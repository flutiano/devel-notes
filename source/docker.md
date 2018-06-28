Docker: the container engine
============================

## Docker Architecture
[Understand the architecture](http://docs.docker.com/introduction/understanding-docker/)

## Docker Tools
  * [Docker Machine](https://docs.docker.com/machine/) 

## Docker Documents
  * [Awesome Docker](https://github.com/veggiemonk/awesome-docker)
  * [Docker Cheet Sheet](https://github.com/wsargent/docker-cheat-sheet)

Usage examples
==============

Docker can be used to run short-lived commands, long-running daemons
(app servers, databases, etc.), interactive shell sessions, etc.

You can find a [list of real-world
examples](https://docs.docker.com/examples/) in the
documentation.

Under the hood
--------------

Under the hood, Docker is built on the following components:

* The
  [cgroups](https://www.kernel.org/doc/Documentation/cgroups/cgroups.txt)
  and
  [namespaces](http://man7.org/linux/man-pages/man7/namespaces.7.html)
  capabilities of the Linux kernel
* The [Go](https://golang.org) programming language
* The [Docker Image Specification](https://github.com/docker/docker/blob/master/image/spec/v1.md)
* The [Libcontainer Specification](https://github.com/opencontainers/runc/blob/master/libcontainer/SPEC.md)

Contributing to Docker
======================

[![GoDoc](https://godoc.org/github.com/docker/docker?status.svg)](https://godoc.org/github.com/docker/docker)
[![Jenkins Build Status](https://jenkins.dockerproject.org/job/Docker%20Master/badge/icon)](https://jenkins.dockerproject.org/job/Docker%20Master/)

Want to hack on Docker? Awesome! We have [instructions to help you get
started contributing code or documentation](https://docs.docker.com/project/who-written-for/).

These instructions are probably not perfect, please let us know if anything
feels wrong or incomplete. Better yet, submit a PR and improve them yourself.

Getting the development builds
==============================

Want to run Docker from a master build? You can download 
master builds at [master.dockerproject.org](https://master.dockerproject.org). 
They are updated with each commit merged into the master branch.

Don't know how to use that super cool new feature in the master build? Check
out the master docs at
[docs.master.dockerproject.org](http://docs.master.dockerproject.org).

How the project is run
======================

Docker is a very, very active project. If you want to learn more about how it is run,
or want to get more involved, the best place to start is [the project directory](https://github.com/docker/docker/tree/master/project).

We are always open to suggestions on process improvements, and are always looking for more maintainers.

### Talking to other Docker users and contributors

<table class="tg">
  <col width="45%">
  <col width="65%">
  <tr>
    <td>Internet&nbsp;Relay&nbsp;Chat&nbsp;(IRC)</td>
    <td>
      <p>
        IRC a direct line to our most knowledgeable Docker users; we have
        both the  <code>#docker</code> and <code>#docker-dev</code> group on
        <strong>irc.freenode.net</strong>.
        IRC is a rich chat protocol but it can overwhelm new users. You can search
        <a href="https://botbot.me/freenode/docker/#" target="_blank">our chat archives</a>.
      </p>
      Read our <a href="https://docs.docker.com/project/get-help/#irc-quickstart" target="_blank">IRC quickstart guide</a> for an easy way to get started.
    </td>
  </tr>
  <tr>
    <td>Google Groups</td>
    <td>
      There are two groups.
      <a href="https://groups.google.com/forum/#!forum/docker-user" target="_blank">Docker-user</a>
      is for people using Docker containers.
      The <a href="https://groups.google.com/forum/#!forum/docker-dev" target="_blank">docker-dev</a>
      group is for contributors and other people contributing to the Docker
      project.
    </td>
  </tr>
  <tr>
    <td>Twitter</td>
    <td>
      You can follow <a href="https://twitter.com/docker/" target="_blank">Docker's Twitter feed</a>
      to get updates on our products. You can also tweet us questions or just
      share blogs or stories.
    </td>
  </tr>
  <tr>
    <td>Stack Overflow</td>
    <td>
      Stack Overflow has over 7000K Docker questions listed. We regularly
      monitor <a href="https://stackoverflow.com/search?tab=newest&q=docker" target="_blank">Docker questions</a>
      and so do many other knowledgeable Docker users.
    </td>
  </tr>
</table>

### Legal

*Brought to you courtesy of our legal counsel. For more context,
please see the [NOTICE](https://github.com/docker/docker/blob/master/NOTICE) document in this repo.*

Use and transfer of Docker may be subject to certain restrictions by the
United States and other governments.

It is your responsibility to ensure that your use and/or transfer does not
violate applicable laws.

For more information, please see https://www.bis.doc.gov


Licensing
=========
Docker is licensed under the Apache License, Version 2.0. See
[LICENSE](https://github.com/docker/docker/blob/master/LICENSE) for the full
license text.

Other Docker Related Projects
=============================
There are a number of projects under development that are based on Docker's
core technology. These projects expand the tooling built around the
Docker platform to broaden its application and utility.

* [Docker Registry](https://github.com/docker/distribution): Registry 
server for Docker (hosting/delivery of repositories and images)
* [Docker Machine](https://github.com/docker/machine): Machine management 
for a container-centric world
* [Docker Swarm](https://github.com/docker/swarm): A Docker-native clustering 
system
* [Docker Compose](https://github.com/docker/compose) (formerly Fig): 
Define and run multi-container apps
* [Kitematic](https://github.com/kitematic/kitematic): The easiest way to use 
Docker on Mac and Windows

If you know of another project underway that should be listed here, please help 
us keep this list up-to-date by submitting a PR.

Awesome-Docker
==============
You can find more projects, tools and articles related to Docker on the [awesome-docker list](https://github.com/veggiemonk/awesome-docker). Add your project there.
