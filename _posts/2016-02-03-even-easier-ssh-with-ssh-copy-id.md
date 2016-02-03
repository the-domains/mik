---
inFeed: true
hasPage: true
inNav: false
inLanguage: null
starred: false
keywords: []
description: ''
datePublished: '2016-02-03T03:56:10.085Z'
dateModified: '2016-02-03T03:55:44.735Z'
authors: []
publisher:
  name: null
  domain: null
  url: null
  favicon: null
title: Even easier ssh with ssh-copy-id
author: []
sourcePath: _posts/2016-02-03-even-easier-ssh-with-ssh-copy-id.md
published: true
url: even-easier-ssh-with-ssh-copy-id/index.html
_type: Article

---
# Even easier ssh with ssh-copy-id

There's an awesome unix utility called`ssh-copy-id`that installs your public key into a remote machine's authorized\_keys file. Before I knew it existed, I was constantly looking up the command I outlined in my previous post[here][0].

If you're using OSX you can install it through homebrew`brew install ssh-copy-id`.

Use the`-i`flag to specify what identify file you want to be copied.

This is way better than how I used to do it:

When you don't give a specific identity file with`-i`, ssh-copy-id will try to login with each key that is output by`ssh-add -L`and add the ones that fail to the`authorized_keys`file on the remote host.

You can see what will happen without making any changes by doing a dry run with the`-n`flag.

[0]: http://michaelpfister.com/code/2013/08/08/seamless-ssh-aliases-and-passwordless-login.html