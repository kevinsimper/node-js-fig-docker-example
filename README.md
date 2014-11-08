node-js-fig-docker-example
==========================

A example on how to use node.js with fig.sh

First install Fig.sh - 
http://www.fig.sh/install.html

Then you can do
```
fig up
```

That will pull down the relevant images and start a web container with a connected mysql database

You can connect to that database via the hostname `db`.

Do you want to look inside either of the machines, you can start a new with
```
fig run web /bin/bash
```
