# MicroContentTestHost

## What
This is a simple sample host page to test [MicroContentViewers](https://microcontent.github.io/).
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
1. go to your commandline and type: `npm install http-server -g`
2. download this index.html to a folder, open a commandline in that folder and run `http-server . -p 5001 --cors`
3. create the index file of your MicroContentViewer in a folder, open a commandline in that folder and run `http-server . -p 5000 --cors`
4. open a browser and enter: http://localhost:5001/?data={%22title%22:%20%22my%20title%22}&url=http://localhost:5000
5. edit the data query parameter as needed

## Where

To make it even easier I host a version of this static index.html on my website at http://goeschlberger.com/microcontent

Working examples:
* [Preview of BinaryNumberContentViewer](http://www.goeschlberger.com/microcontent/?data={%22title%22:%22test%22,%22number%22:12}&url=https://raw.githubusercontent.com/MicroContent/BinaryNumberContentViewer/2e8055272880ce5ba30175240aa18721addf140c/index.html)
* [Preview of KFOX Multiple Choice Multi Select](http://www.goeschlberger.com/microcontent/?data=%7B%22title%22%3A%22title%22%2C%22priority%22%3A1%2C%22type%22%3A%22MCMS%22%2C%22question%22%3A%22question%22%2C%22answers%22%3A%5B%7B%22value%22%3A%22a%22%2C%22correct%22%3Afalse%2C%22lastEdit%22%3A1510331969887%2C%22id%22%3A1%7D%2C%7B%22value%22%3A%22b%22%2C%22correct%22%3Atrue%2C%22lastEdit%22%3A1510331969887%2C%22id%22%3A2%7D%2C%7B%22value%22%3A%22c%22%2C%22correct%22%3Afalse%2C%22lastEdit%22%3A1510331969887%2C%22id%22%3A3%7D%5D%2C%22questionContext%22%3A%22thesecondoption%3F%22%2C%22answerContext%22%3A%22because%22%2C%22lastEdit%22%3A1510331969887%2C%22id%22%3A0%2C%22lessonId%22%3A0%2C%22releaseStatus%22%3A%22PUBLIC%22%2C%22editable%22%3Anull%2C%22learningStatus%22%3A0%2C%22skipStatus%22%3A%22NEVER_SKIPPABLE%22%2C%22multimedia%22%3A%5B%5D%7D&url=https://raw.githubusercontent.com/MicroContent/KFoxMcmsContentViewer/bfffa8ab8344e3dbb4775de6aaaefa408e0f27aa/index.html)

pro tip: You can use your browsers developer console and enter `encodeURIComponent('{ "title": "whatever my json-data looks like"}')`  
