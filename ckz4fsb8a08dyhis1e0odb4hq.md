## How to Terminate a Node Process

You might find yourself managing multiple node processes at the same time while working on a full-stack application. Automated scripts or programs that watch and execute your unit-tests while you code/TDD are possibilities. There is likely Webpack running and serving your frontend on localhost and a node app serving the REST API your frontend is connecting to. Each of these processes would occupy a specific port.

I currently host my React App on localhost:3000 and run my backend on localhost:3001 via serverless offline.

In most cases, you would start those processes from the command line like this:


```npm run react-scripts start```  or ```sls offline start --port 3001``` 

If you run those, you can quickly end them with:


``` Ctrl + C``` 

There has been no issue until now. Occasionally, though, you start a process, and then close the IDE or Terminal, and the process continues to run. When you attempt to restart the process, however, you receive an error saying that the port is busy.

The reason or how this happens is that every now and then (weeks or months) I find myself looking up commands that I don't use very often (and that I can google in under 20 seconds), without knowing why or how I did it. Hence, I'll put it here, it might be useful to others as well.

Thanks to an npm package, [kill-port](https://www.npmjs.com/package/kill-port), I got exactly what I needed with a much more user-friendly interface. The npx package is already installed, so I don't need to do anything. All I need to do is:


```npx kill-port 3000``` 

That's all! Because npx has to temporarily install the kill-port package, it is slower than kill + lsof. However, I can tell you its 100x better. Based on my review of kill-port's source code, it is built on kill + lsof. In my opinion, kill-port provides a more approachable abstraction. 

If for some reason you need to install kill-port npm package, you can use the following command:


```npm i kill-port``` 


