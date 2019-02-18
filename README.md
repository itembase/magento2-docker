# Magento2 Docker Compose set

Docker set for running Magento2 instances.

## Requirements

- Git
- Latest Docker 
- Latest Docker Compose

## How to use

In terminal application clone current repository:

`git clone git@github.com:itembase/magento2-docker.git`

Change to the directory of the repository and switch to the folder of the desired Magento2 version:

`cd magento-xx`

where `xx` can be `21`, `22` or `23`. In that folder run the following command:

`docker-compose up -d`

Wait while all containers will be up and running. As soon as all is up and running run the next command:

`docker-compose exec magento install-magento`

If you wish to have sample data (please note for version 2.2 it does not work at the moment) execute the second command:

`docker-compose exec magento install-sampledata`

When all commands were executed you can visit `http://localhost:300xx` to see store front-end or 
`http://localhost:300xx/admin` for admin side where `xx` can be `21`, `22` or `23`.

The admin password can be found in `env` file and by default it's:

- username: `admin`
- password: `magentorocks1`

## Reference

Based on https://github.com/alexcheng1982/docker-magento2 Docker images.
