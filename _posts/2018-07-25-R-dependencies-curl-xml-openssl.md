---
layout: post
title: Installing dependencies for curl, XML, openssl for R
date: 2018-07-25
categories: r
---

Every time I set up a new Ubuntu install with R, I am missing the dependencies for `curl`, `XML` and `openssl`.

This command worked on Ubuntu 18.04, R 3.4.4:

```bash
sudo apt install libssl-dev libxml2-dev libcurl4-openssl-dev

```
