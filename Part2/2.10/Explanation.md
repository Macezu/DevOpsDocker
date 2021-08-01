My last button worked but everything else was failing and i noticed that Cors was givine errors. I added the backend enviroment variable - REQUEST_ORIGIN=http://localhost in the docker-compose.yml
file and every button started working. 
