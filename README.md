# URL_Shortener

**Docker Repo:** https://hub.docker.com/repository/docker/ragnarokkar/urlshortener-docker

**Prerequisites**
 - Docker must be installed on the system
 - The test folder must be downloaded

**How to run the docker image**

- Open Docker CLI Run the command **docker run -d -p 8000:5000 ragnarokkar/urlshortener-docker** 
- The API will now run on the port 8000 
- Use the URL http://127.0.0.1:8000/shorten to test the status of deployment , you will recieve message *Must use POST* if its running 
- Open test/index.html and enter a URL to get the shortened link 
- The URLs and their shortened versions are saved in a text file in Docker. 
- Open http://127.0.0.1:8000/ABCDEFG to redirect to a url already saved to the text file.

**How to change ports**

To use a different port change the *port* in the command **docker run -d -p *port*:5000 ragnarokkar/urlshortener-docker** and update the URLs in test/scripts/main.js to use the new port
	
**URL Validation**

The API only considers a URL valid if it has protocol in it. So entries like *google.com* will be considered invalid while *https://google.com* will work.
