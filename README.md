# Lexis Nexis Scraper


## Description

This repository contains a python package for the automated scraping of the Lexis Nexis web service. 

Why use this package/code? There are a small collection of alternative options available however these codesets are either outdated, inefficient, require access to the official API, or are not suitably customisable. These reasons led to the development of this package.  

Currently, this package only works for academic users but the functionality can easily be expanded to regular and organisational users. Please let us know if you want these features incorporated!

Whilst our best efforts have been made to ensure that the package is robust, as with any web scraping tasks connection drop outs, delays in obtaining pages may cause issues. Likewise, if the website structure changes we endeavour to do our best to update the package as soon as an issue is raised. 

> **_DISCLAIMER:_** This code was developed for academic purposes. Using this software package may be a violation of the terms of use set out by LexisNexis. By downloading and using this package you do so at your own legal risk.

## Requirements

- Lexis Nexis Subscription (API Access Not Required)
- Python 3
- Chrome Driver
  - Used to simulate a real web browser.
  - Available to download at: https://chromedriver.chromium.org/downloads
- Access to MySQL Database (Optional)

## Installation

### Using PIP

``` pip install lnscraper ```

### Manual Installation

## Usage

### Authentication Setup
This bot automatically completes the authentication information for an academic sign-in at regular intervals. In order to do this you need to get your institution login link.  

1. Access the Nexis Service by visiting https://nexis.com
2. Click on the academic sign in link. 
3. Find your institution and click “copy link”. 
4. Copy the link within the pop-up box and save it for later!

Whilst the pre-configured options will work in the majority of cases you may need to adjust the following options to ensure that the correct authentication fields are completed.

5. Click the link. 
6. Right Click on the username field and click inspect. Repeat. 
7. If the id=‘username’ do nothing. Else save the id value for later. 
8. Now repeat step 6 for the password field.
9. If the id=‘password’do nothing. Else save the id value for later.

### Credentials File

### Storage Option

The data can either be saved into either a mySQL database or a pandas dataframe. These need to be setup, as follows, before the webscraping can be initiated. 

#### MySQL (Recommended)

```python
from lnscraper import mysql_version, authentication
```

#### Pandas

```python
from lnscraper import pandas_version, authentication
```

### Search Terms and Sources

### Running the WebScraper


## Citing This Package
Please accredit this package by citing the following in your references. 

```
@phdthesis{hammocks_2019, title={Identifying Weak Signals of Future Change: Detecting and Analysing Trends in Modus Operandi Through Topic Modelling}, author={Hammocks, Daniel}, year={2019}}
```
