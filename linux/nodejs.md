
In this class we will understand Nodejs installtion and how to start Nodejs server and access it.

Nodejs is an event-driven programming for webservers

Installing nodejs
```
sudo apt update - this command will update package index and not the package itself, to update the package with latest version you need to use apt-get install command

sudo apt install nodejs - this will install latest version of nodejs
```

Check node version

```
node -v
```

Install npm - it is used to install modules and packages to use with Node.js (Node Package Manager)

```
sudo apt install npm - for ubutnu we use apt-get and for macos we use brew simillarly we use npm for nodejs
```

Create a project folder and app.js file

```
mkdir first-node-project
cd first-node-project
cat <<EOF
const http = require('http');

const hostname = '0.0.0.0';
const port = 3000;

const server = http.createServer((req, res) => {
  res.statusCode = 200;
  res.setHeader('Content-Type', 'text/plain');
  res.end('Hello World');
});

server.listen(port, hostname, () => {
  console.log(`Server running at http://${hostname}:${port}/`);
});
EOF

```

start node server
```
node app.js &
```

Open browser and type server-ip:3000

to get your systems ip use one of the command 
```
ifconfig || ip a
```

