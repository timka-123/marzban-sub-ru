<p align="center">
  <a href="https://github.com/x0sina/marzban-sub" target="_blank" rel="noopener noreferrer">
    <img src="https://github.com/DigneZzZ/marzban-sub-ru/blob/main/Preview_page.jpeg" height="500px title="Marzba-Sub"/>
  

  </a>
</p>
<h1 align="center"/> <a href="https://github.com/Gozargah/Marzban">Страница подписки для Marzban</a></h1>

# Table of Contents
- [Attributes](#Attributes)
- [Installation Steps](#Install-Steps)
- [Default Language](#Default-Language)
- [Personalization](#Personalization)
- [Host Version](#Host-Version)

# Introduction
A simple html template to better display user information

# Attributes
- Quickly add subscription links to programs
- The link to download the required applications
- Three languages (Russian)
- Sub fantasy page with beautiful color and glaze
- Receive the configs with the copy icon at the bottom of the page
# Installation Steps
1. Download File Template
```sh
sudo wget -N -P /var/lib/marzban/templates/subscription/  https://raw.githubusercontent.com/dignezzz/marzban-sub-ru/main/index.html
```

2. Enter the following commands in your server's terminal:
```sh
echo 'CUSTOM_TEMPLATES_DIRECTORY="/var/lib/marzban/templates/"' | sudo tee -a /opt/marzban/.env
echo 'SUBSCRIPTION_PAGE_TEMPLATE="subscription/index.html"' | sudo tee -a /opt/marzban/.env
```
Or uncomment the following values in `.env` file in `/opt/marzban` folder by removing # at the begining of them.
```sh
CUSTOM_TEMPLATES_DIRECTORY="/var/lib/marzban/templates/"
SUBSCRIPTION_PAGE_TEMPLATE="subscription/index.html"
```

3. Restart Marzban
```sh
marzban restart
```

## Update
To update the template, just repeat step 1.

# Default Language
Default Language only RUSSIAN

In this example, the main language is English.

# Personalization
To personalize the Telegram ID, background image and user logo, changes must be included in the html file, which is possible by searching for some values.
To search using nano, first open the file with nano with the following command:
```
nano /var/lib/marzban/templates/subscription/index.html
```
Then open the search bar with Ctrl + W combination buttons and search for the following phrase to change Telegram support ID:
```
https://t.me/yourID
```
Search for the user's logo:
```
images/marzban.svg
```

## Host Version
To use the host version, upload the sub folder to the host and change the value of BASE_URL to your panel address in the index.php file just like the following example. Remember to write http if you don't have an SSL for your panel domain.
```
const BASE_URL = "https://BaseUrl:PORT";
```

## Copyright
This template is based on <a href="https://github.com/Gozargah/Marzban">Marzban Templates<a> design.
