# MicroContentTestHost

## What
This is a simple sample host page to test MicroContentViewers.
You can provide data and the url to MicroContentViewer as query parameters.

Examples: 
* http://wherever-this-page-is-hosted.com/index.html?data={%20%22number%22:%2012,%20%22title%22:%20%22my%20title%22}&url=https://raw.githubusercontent.com/MicroContent/BinaryNumberContentViewer/2e8055272880ce5ba30175240aa18721addf140c/index.html
* http://localhost:5001/?data={%22title%22:%20%22my%20title%22}&url=http://localhost:5000

## Why
This is a tool for developers of MicroContentViewers.
You can test your MicroContentViewers as you develop by hosting your code locally (e.g. using [http-server](https://www.npmjs.com/package/http-server)).
Don't forget to enable cors!

Easiest setup:
(0. download node.js/npm)
1. go to your commandline and type: npm install http-server -g
2. download this index.html to a folder, open a commandline in that folder and run "http-server . -p 5001 --cors"
3. create the index file of your MicroContentViewer in a folder, open a commandline in that folder and run "http-server . -p 5000 --cors"
4. open a browser and enter: http://localhost:5001/?data={%22title%22:%20%22my%20title%22}&url=http://localhost:5000
5. edit the data query parameter as needed
