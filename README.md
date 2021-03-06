# Hackernews Scraper


*This is a python app and can be used as a web scraper for hackernews site. The app takes one input( a +ive integer) no of posts as an argument.*
*And shows the top no of posts. It also exposes one REST endpoint that can be used with <b>curl</b> command.*
*It uses famous BeautifulSoup to parse the page information and then sub children are extracted.*

*The code is simple and easy to understand. The APP reads the site url from the config.yml file.*


## Run as a standalone application with REST endpoint.
Install python3 and pip on your machine : https://www.python.org/downloads/.<br />
Use a shell/terminal/bash shell window to run the following commands.<br />

```
git clone git@github.com:IamSoo/hackernews-scraper.git
cd hackernews-scraper

pip install virtualenv
virtualenv -p python scrape_env
source scrape_env/bin/activate

pip install -r requirements.txt

```
The above will create the virtualenv and install all our required libraries.<br />

### Unit testing and coverage:</br>
For test and coverage we can use the following syntax:</br>

```
python  hackernewsTest.py

coverage run hackernewsTest.py
coverage report -m
```
### Testing:</br>
To run the script and to see 3 top posts type the following command:
```
python hackernews.py --posts 3

```
To run the REST end point use the following command:
```
python hackernewsEndpoint.py

```
This will run one flask server. To test open a browser and type below :<br/>
http://localhost:5000/hackernews?posts=3

To use curl command to test open a shell/scripting window and type the following :<br/>
curl http://localhost:5000/hackernews?posts=3


## Run as a docker container with REST endpoint
Docker image : https://hub.docker.com/repository/docker/iamsoo/hackernews-scraping

Running docker image:

```
docker run -p 5000:5000 iamsoo/hackernews-scraping

```
### Testing:</br>

This will run one flask server on a container. To test open a browser and type below :<br/>
http://localhost:5000/hackernews?posts=3

To use curl command to test open a shell/scripting window and type the following :<br/>
curl http://localhost:5000/hackernews?posts=3


### Major Libraries Used:

 * beautifulsoup4 : For extracting html
 * json : Handling Json data
 * Flask : Web framework for exposint REST endpoint
 * coverage : For unit test coverage
 * urllib3 : Http client to connect to the website
 * unittest2 : For unit test
 * lxml : HTML/XML parser
 * pyyaml : For handling yaml file(Config file)

