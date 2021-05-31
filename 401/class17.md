# Web Scraping
![](https://www.hirinfotech.com/wp-content/uploads/2019/10/What-is-Web-Scraping.png)

Web scraping, web harvesting, or web data extraction is data scraping used for extracting data from websites. The web scraping software may directly access the World Wide Web using the Hypertext Transfer Protocol or a web browser. While web scraping can be done manually by a software user, the term typically refers to automated processes implemented using a bot or web crawler. It is a form of copying in which specific data is gathered and copied from the web, typically into a central local database or spreadsheet, for later retrieval or analysis.



##  BeautifulSoup
For web scraping we are going to use the very popular Python library called BeautifulSoup.

![](https://letslearnabout.net/wp-content/uploads/2019/08/cooking.png)

### 1. Getting Started:

    pip install beautifulsoup4
    or 
    poetry add beautifulsoup4

### 2. Inspecting
The first step in scraping is to select the website you wish to scrape data from and inspect it. 

To inspect a website right click anywhere on the page and choose ‘Inspect Element’ / ‘View Page Source’ 

### 3. Parsing
Now we can begin parsing the webpage and searching for the specific elements we need using BeautifulSoup. For connecting to the website and getting the HTML we will use Python’s urllib. Let us import the required libraries-

        from urllib.request import urlopen
        from bs4 import BeautifulSoup

3a. Get the url-

    url = "https://www.bbc.com/sport/football/46897172"

3b. Connecting to the website-

        try:
        page = urlopen(url)
        except:
        print("Error opening the URL")

3c. Create a BeautifulSoup object for parsing-

    soup = BeautifulSoup(page, 'html.parser')

### 4. Extracting the required elements:
We now use BeautifulSoup’s soup.find() method to search for the tag 

    content = soup.find('div', {"class": "story-body sp-story-body gel-      body-copy"})

We now iterate through content to find all the <p> (paragraph) tags in it to get the entire body of the article.

        article = ''
        for i in content.findAll('p'):
            article = article + ' ' +  i.text

### 5. Saving the parsed text:
We can save the information we scraped in a .txt or .csv file.

        with open('scraped_text.txt', 'w') as file:
            file.write(article)


## How to scrape websites without getting blocked?
![](https://d33wubrfki0l68.cloudfront.net/3466294555380f62f649e2847f93cd82450bdde7/ccefb/blog/web-scraping-without-getting-blocked/6augn0y6fqtlqd08ratm.png)

1. Respect Robots.txt
2. Make the crawling slower, do not slam the server, treat websites nicely

3. Do not follow the same crawling pattern
4. Make requests through Proxies and rotate them as needed
5. Rotate User Agents and corresponding HTTP Request 6. Headers between requests
6. Use a headless browser like Puppeteer, Selenium or Playwright
7. Beware of Honey Pot Traps
8. Check if Website is Changing Layouts
7. Avoid scraping data behind a login
8. Use Captcha Solving Services
