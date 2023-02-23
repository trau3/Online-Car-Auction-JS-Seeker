<div align="center">

# Online Car Auction JS Seeker



</div>


## Keywords

Section 704, Website, Puppeteer.JS, Web Scraping, Car Auctions

## Project Abstract /  High Level Requirements

This project makes the process of searching for auction cars easier to find. Auctions are a good place to get used cars for a deal, but it’s difficult to find them. The main goal of this project is project is to make a website that makes websites like Copart and IAAI easier to use and assign working alerts to it. Users can search for items that may be listed and apply special filters to make their search easier. If there is enough time, more features will be added for other auction websites too so users can search through multiple websites at once. Users can subscribe to receive alerts when something new is posted.


## Conceptual Design

The main concept will be a website with a main search screen that provides extra filters/options when needed. A location will be provided for the user to enter as well as the distance to search from. The user will have the option to save the search and receive alerts whenever a new listing is added. This data can be stored in a SQL server to send email alerts and provide data about listed items. When a user searches, puppeteer (a Node.js library) scrapes data from the website and displays it to the user.
The project will be based on https://github.com/ovdixon/marketplace-magpie, but this repository handles Facebook Marketplace. Facebook Marketplace can’t be scraped due to scraping being against the terms of service, but a fork of this repository was made for IAAI.com. More capabilities for other marketplaces will need to be developed. There is no UI, so this a website will need to be developed for users to interact. This can be done through one of the JavaScript libraries for websites. 



## Background
There is one closed-source website like this proposed project, which is search tempest and auto tempest. In this website, it compiles a list of items from multiple marketplaces, but it does not generate information surrounding car auctions. Car auctions offer the benefit of getting a car for a lower price than it would be if it were sold at a dealership. In this project, the results will be directly displayed on the website by scraping the auction websites for the data. There are some websites that already scrape data from IAAI and Copart, but they cost money and there is no UI. One benefit this website will provide is features like filtering out states that require a broker to make it easier to find the right auction car.


## Required Resources

To develop this project, a server will be needed to keep the website running. One suggestion for this is to use a free Oracle server. Overall knowledge of JavaScript and Puppeteer JS is needed to parse the websites for the data. Knowledge of the limitations of certain websites will be needed when scraping, which can be found by putting looking at the {website address}/robots.txt file. Knowledge of building a website will be needed. A framework for the website will need to be chosen. Some SQL knowledge will need to be obtained as well. A UML diagram of the website will be needed for documentation.

## Proof of concept
A forked repository was made that uses Node.js and puppeteer to get the info from IAAI.com. The script generates a screenshot of the website, but no data has been parsed yet. There are commented sections of code that show data parsing for Facebook Marketplace:
https://github.com/trau3/marketplace-magpie

To run the program, Node.js must be installed. It can be downloaded here:
https://nodejs.org/en/download/

There are multiple libraries needed, which can be installed using the following command inside the directory of the cloned repository:
npm i

After that, users can just run the program using the following command:
node scrape.js

This was built on a Windows 10 machine with Node.js v19.2.0, but it should work with other platforms. 
The output should be two images showing the website for the two searches done. These will need to be parsed for data in the future.
