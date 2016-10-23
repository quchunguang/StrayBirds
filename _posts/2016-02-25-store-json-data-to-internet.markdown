---
layout: post
title: store json data to internet
categories: [tech]
tags: [myjson, json]
published: True
comments: True
---

curl -s https://api.myjson.com/bins/1p2z7
200 OK
{"app_name":"Helloworld","version":"1.0"}

curl -H "Content-Type: application/json" -X POST -d '{"username":"xyz","password":"xyz"}' https://api.myjson.com/bins
201 Created

curl -H "Content-Type: application/json" -X PUT -d '{"password":"abc"}' https://api.myjson.com/bins/200hv
200 OK

[1]: http://myjson.com/api
