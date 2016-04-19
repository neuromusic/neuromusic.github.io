---
layout: post
title: "Zero Configuration Remote Jupyter Server"
tags:
    - python
    - jupyter
disqus: True
image: Portrait_of_Jupiter_from_Cassini.jpg
---
My personal laptop has a modest 4 core CPU, only 4 gigs of RAM and a 256GB hard drive. One of the servers in our lab, on the other hand, has 24 cores, 128GB of RAM, a 20TB file server, two Nvidia Tesla K40s, and one Titan Z GPU.

Which would you prefer to run your analyses on?

A while ago I set up [Jupyter/IPython notebook servers for each user](https://github.com/neuromusic/ipynb-deploy) on our lab server. It hides them behind an nginx server, giving everyone a URL to access their notebooks that run on the server. It works, but there's quite a bit of overhead involved (supervisord, nginx, etc).

The [new postdoc](https://github.com/zekearneodo) in the lab showed me a way easier way to run a notebook remotely w/ no overhead. No nginx, no firewall configuration, and as secure as ssh. And now I'm going to show you.

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

This approach is incredibly flexible... as long as you can open up an ssh connection to the server, you can run your notebook on the server using your browser as the interface:

<blockquote class="twitter-tweet tw-align-center" data-conversation="none" data-lang="en"><p lang="en" dir="ltr"><a href="https://twitter.com/neuromusic">@neuromusic</a> As of now I can also confirm this method works for ssh-ing into Amazon EC2 instances, even with a key-pair.</p>&mdash; Grant (@usethespacebar) <a href="https://twitter.com/usethespacebar/status/701235455006617600">February 21, 2016</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

This opens up tons of possibilities...

- If you use multiple Python environments on your server (say, one for each project), this methods lets you easily easily switch between them.
- Even if you don't have a headless server you need to connect to, maybe you are on a 5 hour flight and want to connect back to your workstation in the office. Easy peasy.

Try it. Let me know how it goes.