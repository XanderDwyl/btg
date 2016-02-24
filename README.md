# Buanga This Guy

![build_status](https://api.travis-ci.org/wadiwasi/btg.svg?branch=master)

## Setup Dev Environment

To get started right away, just install the following:

1. [Docker](https://docs.docker.com/engine/installation/)
2. [Docker Compose](https://docs.docker.com/compose/install/)
3. [Docker Machine](https://docs.docker.com/machine/install-machine/)

### Setup on Mac

**Requirements**

- [VirtualBox](https://www.virtualbox.org/wiki/Downloads) for docker-machine driver.
- The super duper extra mega ultra awesome package manager for mac, -=[ [Brew](http://brew.sh/) ]=- !

&nbsp;

**Install 'em all!**

1. `$ brew update && brew install docker docker-compose docker-machine`

    > Once you're done, you need to provision a boot2docker virtual machine.

2. Provision a new machine with **`2048 MB`** of RAM

    `$ docker-machine create -d virtualbox --virtualbox-memory "2048" dev`

3. Activate docker environment with the newly created box

    `$ eval $(docker-machine env dev)`


    > Check if everything's fine by running `$ docker ps` or `$ docker images`. If
    there's no error, then you're good to go.

&nbsp;

## Provisioning (docker-compose)

Once your docker env is all set up, then you're pretty much ready to get your hands all dirty. So let's get crackin`!

1. **First off, run the following:**

    **`$ make sandwich`**
    >
    > `$ make sandwich` is just a wrapper of `$ make compose` which is also a wrapper to `$ docker-compose up` but with added sugar to make our lives a tad bit easier.
    >
    
    &nbsp;  
    
    > **This command should:**
    
    > 1. Create a random password exported as `BTG_PASS` for `redis` and `mongodb`
    > 2. Set up mongodb && redis store _ENV VARS_ for  _URL_
    > 3. Provision the containers
    
    &nbsp;
    
2. **Next should be:**

    **`$ make setup`**
    >
    > This will copy some commit-hook scripts to `.git/hooks` folder.
    
    &nbsp;

## Development

- **Stack - Please read their corresponding documentation.**
    - [Swig](http://paularmstrong.github.io/swig/) - Templating Engine
    - [Koa](http://koajs.com) - Main Framework
    - _Will add more later..._
- **Auto run tests**
	- Run `$ make tdd`
	- Write your code ( watchers will auto run the tests for you )
- **Auto reload server**
	- Run `$ make server`
	- Write your code ( watchers will... yup! )

&nbsp;

## Contributing

> For now, there isn't any solid set of rules or conventions yet, maybe later will add it in here. For the time being, you can just write your code as you please and submit pull-request so others can review.
>
> more later...

**Can someone please do something about the following?**

- Code Convention
- Stack docs
- What else?
