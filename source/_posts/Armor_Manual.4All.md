---
title: Armor_Manual.4ALL.md
date: 2016-10-13 10:07:01
tags:
  - All
categories:
  - Estuary
  - Documents
  - All
---
* [Introduction](#1)
* [Information of Supported Armor Tools ](#2)
* [Distributions](#3)
* [Installation](#4)
* [How to run Tool's test scripts](#5)
<!--more-->

## <a name="1">Introduction</a>

Armor tools supports a list of the platform tools for debug, diagnostics and monitoring and those are available in Open-Estuary Solution.

Current Release Version- `armor-v1.1`

## <a name="2">Information of Supported Armor Tools</a>

For the supported tools in Armor on different distributions, please refer  https://github.com/open-estuary/estuary/blob/master/doc/Armor_Tools_Supported.4All.md

For the basic information of all the supported Armor tools please refer https://github.com/open-estuary/estuary/blob/master/doc/Armor_Tools_Basic_Info.4All.md

Documentation for L3 cache event counting support in perf https://github.com/open-estuary/estuary/blob/master/doc/README.armor.perf.md

Documentation for using KGDB and KDB please refer https://github.com/open-estuary/estuary/blob/master/doc/README.armor.kgdb.kdb.md

Documentation for LTTng user space tracing and kernel tracing, please refer https://github.com/open-estuary/estuary/blob/master/doc/README.armor.lttng.md

Documentation for how to verify iptables tool, please refer https://github.com/open-estuary/estuary/blob/master/doc/README.armor.iptables.md

## <a name="3">Distributions</a>

Presently Armor tools are supported on the following distributions.

* Ubuntu 15.04 ARM64  
* Fedora 22 ARM64  
* OpenSuse 20150813 Tumbleweed ARM64  
* Debian Jessie 8.2 ARM64  
* CentOS Linux release 7.2.1511 (AltArch)  

## <a name="4">Installation</a>

1. Default Armor tools are installed onto the rootfs during open-estuary build process.  
2. On first time bootup, user must run update commands before try install or run any Armor tool.

   Ubuntu: run `apt-get -y update` command.  
   Fedora: run `dnf -y update` command.  
   OpenSuse: run `zypper -y update` command.  
   Debian: run `apt-get -y update`and `apt-get install -f -y` commands.  
   CentOS: run `yum -y update` command.  
3. On target board, Run `armor_utility`, which will provide information of the supported Armor tools, installation status and how to install on the distribution if it is not already present.

## <a name="5">How to run Tool's test scripts</a>

1. Go to the `/usr/local/armor/test_scripts` on the target terminal.  
2. To test individual tools please run folowing command on the shell terminal, `sh test_<tool's name>.sh` -> to run test script of an armor tool.
    For example, 'sh test_strace.sh' to run tests for strace. The test results can be seen on the console.
