---
layout: post
title: "Import GPG keys"
description: "Resolve GPG Error when apt-get update"
category: Linux
tags: [GPG Linux]
---
{% include JB/setup %}

## Issue desc
I want to install debs which not exist in ubuntu org source list, So I add the not org source to sources.list. But when I apt-get update, I got the `GPG Error` about missing public key. then Google it.

    W: GPG error: http://download.tuxfamily.org ./ Release: The following signatures couldn''t be verified because the public key is not available: NO_PUBKEY __73E6B0FAA42A6CF5__  

## Fix Steps
GPG public key is used to verified the debs from source list, so need to recv and import it from public keyserver.  
Here are some public keyservers:  

    http://keyserver.ubuntu.com
    http://pgp.mit.edu/ 
    http://wwwkeys.pgp.net 
    http://subkeys.pgp.net

__1. recv GPG public key__

    $ gpg --keyserver pgp.mit.edu --recv-keys 73E6B0FAA42A6CF5
    gpg: requesting key A42A6CF5 from hkp server pgp.mit.edu
    gpg: /root/.gnupg/trustdb.gpg: trustdb created
    gpg: key A42A6CF5: public key "shame (beryl repository) <shame@sidux>" imported
    gpg: no ultimately trusted keys found
    gpg: Total number processed: 1
    gpg:               imported: 1

__2. import public key into apt__

    gpg --armor --export 73E6B0FAA42A6CF5 | apt-key add -

__3. apt-get update again__

<<EOF

