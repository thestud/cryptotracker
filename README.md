# cryptotracker
A pie chart that shows the percentages of the market of the crypto currencies in Vue JS accessing my example go test API

Note: this instructions are linux based

prerequisites:
	1. npm  installing linux: https://linuxize.com/post/how-to-install-node-js-on-ubuntu-18.04/
	2. npm install vue https://vuejs.org/v2/guide/installation.html 
	3. npm install on directory
	4. npm install --save axios https://medium.com/spemer/using-axios-in-vue-js-17f186756a8b

to run:
	1. npm run dev


to build docker image: 
	Windows and Mac Os:
		docker build -t cryptotracker .
	Linux:
		sudo docker build -t cryptotracker .

to run docker image:
	Windows and Mac Os:
		docker run -p 8080:8080 cryptotracker
	Linux:
		sudo docker run -p 8080:8080 cryptotracker

to find container name:
	Windows and Mac Os:
		docker ps
	Linux: 
		sudo docker ps

to stop docker image:
	Windows and Mac Os:
		docker stop <container name>
	Linux:
		sudo docker stop <container name> 


to change ip address or port:
	1. change line in App.vue axios.get('http://localhost:4000/cryptos')

