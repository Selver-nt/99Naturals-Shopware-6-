# Naturals

## Introduction

Shopware theme

## Installation

Clone the development template:
```bash
git clone https://github.com/shopware/development.git
```
Now navigate into it:
```bash
cd development
```
Remove the existing platform directory: 
```bash
rm -rf platform
```
and then clone new one: 
```bash
git clone https://github.com/shopware/platform.git
```

At least on Linux operating systems, docker installation is the easiest way to get a running Shopware 6. This way you can set up Shopware 6 with just three easy commands:
1. Build and start the containers:
```bash
./psh.phar docker:start
```
2. Access the application container:
```bash
./psh.phar docker:ssh
```
3. Execute the installer inside the docker container:
```bash
./psh.phar install
```

To be sure the installation succeeded, just open the following url in your favorite browser: http://localhost:8000/

Stop project in two easy steps: 
1. Leave the shell:
```bash
exit
```
2. Stop the containers:
```bash
./psh.phar docker:stop
```

## Configuration
In order to have the same look as in the design, it is necessary to adjust the setting in the admin:

Setting > Products > show reviews => disable
Setting > System > Custom fields => {
    Tehnical name => custom_product_fields
    Label => Product custom field
    Asign to => Products

    Custom field => {
        Tehnical name => custom_product_fields_natural_icons
        Type => Active switch
        Label => Natural icons
    }
}