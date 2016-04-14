---
layout: post
title: "Zero Configuration Remote Jupyter Server"
tags:
    - python
    - jupyter
disqus: True
image: Portrait_of_Jupiter_from_Cassini.jpg
---

A while ago I set up [Jupyter/IPython notebook servers for each user](https://github.com/neuromusic/ipynb-deploy) on our lab server. It hides them behind an nginx server, giving everyone a URL to access their notebooks. It works, but there's a bit of overhead involved (supervisord, nginx, etc).

However, the new postdoc in the lab showed me a way easier way to run a notebook remotely w/ no overhead. No nginx, no firewall connection, and as secure as ssh. And now I'm going to show you.

Login to your server via ssh, then fire up a jupyter notebook w/ &quot;no-browser&quot; and give it a port:

``` bash 
jupyter notebook --no-browser --port=8888
```

So now you have a jupyter notebook running on your server at localhost:8888

Next, ssh into the server and forward a local port to the server's port where jupyter is running:

``` bash
ssh -NL 8888:localhost:8888 username@server
```

Now, open your browser and go to localhost:8888 and BAM you've got your remote jupyter server in your browser.

<blockquote class="twitter-tweet tw-align-center" data-conversation="none" data-lang="en"><p lang="en" dir="ltr"><a href="https://twitter.com/neuromusic">@neuromusic</a> As of now I can also confirm this method works for ssh-ing into Amazon EC2 instances, even with a key-pair.</p>&mdash; Grant (@usethespacebar) <a href="https://twitter.com/usethespacebar/status/701235455006617600">February 21, 2016</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>
