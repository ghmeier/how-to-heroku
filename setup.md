# Setup
Aka, things you'll need for to get going.

### What you'll need
* git
* heroku toolbelt
* nodejs
* npm

## Let's get Started
First we'll install git.

### Installing git
git is a version control system, like Google docs on steroids.
You can follow GitHub's tutorial [here](https://help.github.com/articles/set-up-git).

1. [Create a github account](https://github.com/join)
2. Download and install github:

__Windows__
  * Download and install [github desktop](https://desktop.github.com)

__Mac__
  * Download and install [the latest version of git](http://git-scm.com/downloads)

__Linux__
  * Install the latest version of git: 
   * `sudo apt-get install git`
   * `sudo dnf install git`

####Let's test it
```shell 
$ git version
git version 2.4.3
 ```
#### Creating a repository
Set up your local git to know who you are:
`$ git config --global user.name "Jane Programmer"`
`$ git config --global user.email "jane@hackisu.com"`

Create a new repository on GitHub, let's name it 'hello-world.'

Now, we can clone it:
`$ git clone https://github.com/<github-username>/hello-world.git`
`$ cd hello-world`

### Installing Heroku Toolbelt

1. Make a [heroku account](https://signup.heroku.com/)
2. Install the heroku toolbelt:

__Windows and Mac__
  * Download and install from [here](https://devcenter.heroku.com/articles/getting-started-with-nodejs#set-up)

__Linux__
  * Install the latest version: `$ sudo wget -O- https://toolbelt.heroku.com/install-ubuntu.sh | sh`
  
Login to the heroku toolbelt, `$ heroku login` using your Heroku username and password. 

Now, we'll create our heroku app:
```
$ heroku create <github-username>-hello-world
Creating ghmeier-hello-world... done, stack is cedar-14
https://ghmeier-hello-world.herokuapp.com/ | https://git.heroku.com/ghmeier-hello-world.git
```

#### Let's install node

1. Install node:

__Windows and Mac__

Download latest [Node Installer](https://nodejs.org/en/download/) and run it.

__Linux__

Run these commands:
* Fedora, Centos:
```
$ curl --silent --location https://rpm.nodesource.com/setup_4.x | bash -
$ dnf -y install nodejs
```
* Debian, Ubuntu:
```
curl -sL https://deb.nodesource.com/setup_4.x | sudo -E bash -
sudo apt-get install -y nodejs
```

2. Test it out:
```
$ node -v
v4.3.0
```

#### Almost there, install node package manager (npm)

1. `npm install npm -g`

*We're done! [Let's start makimg some files](/making-the-app.md)!*
