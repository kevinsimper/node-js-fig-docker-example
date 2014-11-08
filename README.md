# Node.js fig.sh example

A example on how to use node.js with fig.sh

First install Fig.sh - 
http://www.fig.sh/install.html

Then you can do
```
fig start
```

That will pull down the relevant images and start a web container with a connected mysql database

You can connect to that database via the hostname `db`.

Do you want to look inside either of the machines, you can start a new with
```
fig run web /bin/bash
```

## Restart on file changes

Because we are using VirtuelBox, we can not use file system events, like a event for a file change.

To make that work, install `nodemon` outside on your own computer
```
npm install nodemon -g
```

Then you first do
```
fig start
```
to start all the services.

Then you run the nodemon deamon with the following, that will restart the web node every time something change
```
nodemon --exec "fig restart web"
