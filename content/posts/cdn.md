+++
draft = false
date = 2023-08-31
title = "CDN"
description = ""
tags = ["Computer Network","System Design"]
+++

* [Definition](#definition)
* [CDN Push](#cdn-push)
* [CDN Pull](#cdn-pull)

## Definition
CDN (**Content Delievery Network**) is a group of **cache server** spread all over the world so that they can cache content close to users.

By using a CDN, Not only can data be accessed faster than fetching it from origin server (latency badly influences user experience), but also reduce the load for origin server.

It is also worth to be noted that, if some CDN servers are down due to hardware failure, companies may have other servers that are near to user which won't affect user to access content.


## CDN Push
Once new data is added to origin server, it is **immediately** pushed to all of the cache servers.

A good example of the use of CDN push is website like youtube. User do not have to wait until content is transfered from the origin server to the CDN. Every request as user make leads to a **cache hit**.

## CDN Pull
If the data is not in CDN, cache server will bed checked first. If it is still not found, the cache server will retrieve it from origin server.

Pull here means that comparing to push, CDN is pulling data from origin server on a in need base. That is to say,
instead of having all content in every CDN, we can have data that is most accesed by people in that region. In this way, we reduce the burden for the origin server.

For example, Twitter has feature like `Trend`. If you are in Japan, you may want to see content in Japanese which are more popular there. In this case, for servers in Japan, they might have more content in Japanese rather than English content. For regions like US, servers may contains more English content instead.
