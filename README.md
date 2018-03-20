# DSAL bash script to create Magento projects using Docksal

This is a simple bash script which uses the Docksal Magento container and creates a light environment.

## Features
- Setup a Magento 1/2 project within minutes
- Import an existing Magento 1.x project by importing a .sql file
- Import an existing Magento 2.x project by importing a .sql file


## Requirements
- Docker installed
- Docksal installed

## Installation
### Global

Execute the following command in your terminal in order to execute the installer. You need to have "git" and "curl" installed within your terminal.

	bash <(curl -s -X GET "https://raw.githubusercontent.com/fsspencer/docksal-dsal/master/dsal?v='$(date +"%s")'") setup

This will install the `dsal` command in ~/.dsal/bin and create a symlink on the /usr/local/bin directory.


## Usage

     dsal <action> <arguments...>

Actions:

| Command | Description |
| ------- | ----------- |
||
| **init** | *Initialize Magento project* |
| **bash** | *Connect to your docker container* |
||
| **php** | *Executes php cli within your project root* |
| **composer** | *Executes composer within your project root* |
| **npm** | *Executes npm within your project root* |
| **n98** | *Executes n98-magerun within your project root* |
| **magento** | *Executes Magento 2 command line tool (e.g: dsal magento setup:upgrade)* |
||
| **setup** | *Installs dsal command locally on your computer* |
| **self-update** | *Updates dsal locally on your computer* |
| **permissions** | *Resote magento file system permissions* |


**NOTE:** All of this commands will work only for your project root directory. That means that if you want to use, for example, gulp on a specify directory within project project (e.g.: skin/frontend/myvendor/mytheme/) it won't work. In that case, you will need to use the "fin bash" command and navigate to that directory and use the gulp command from that place.

## Credits
- Francis S. Spencer - <francis.s.spencer@gmail.com>
- codealist.net
