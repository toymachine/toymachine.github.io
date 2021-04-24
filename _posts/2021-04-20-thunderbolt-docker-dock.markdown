---
layout: post
title:  "Thunderbolt Docker Dock"
date:   2021-04-20 13:05:27 +0200
categories: development environment
---
You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve`, which launches a web server and auto-regenerates your site when a file is updated.

Jekyll requires blog post files to be named according to the following format:

`YEAR-MONTH-DAY-title.MARKUP`

Where `YEAR` is a four-digit number, `MONTH` and `DAY` are both two-digit numbers, and `MARKUP` is the file extension representing the format used in the file. After that, include the necessary front matter. Take a look at the source for this post to get an idea about how it works.

Jekyll also offers powerful support for code snippets:

bursty load, quit fan (fanless, 22 ambient, around 41% idle cpu)
	Ubuntu 20.10 (server)
  32GB



{% highlight yaml %}
network:
  ethernets:
    eno1:
      dhcp4: true
      optional: true
    thunderbolt0:
      dhcp4: false
      addresses: [192.168.3.4/24]
      routes:
        - to: 192.168.3.1
          via: 192.168.3.1
      optional: true
{% endhighlight %}

{% highlight shell %}
 06:59 PM ~ ] iperf -c 192.168.3.4
------------------------------------------------------------
Client connecting to 192.168.3.4, TCP port 5001
TCP window size:  129 KByte (default)
------------------------------------------------------------
[  4] local 192.168.3.1 port 62556 connected with 192.168.3.4 port 5001
[ ID] Interval       Transfer     Bandwidth
[  4]  0.0-10.0 sec  17.7 GBytes  15.2 Gbits/sec
{% endhighlight %}


Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
