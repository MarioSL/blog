---
layout: post
title: "How to install Ruby on Rails on Ubuntu 18.04 from scratch quickly"
date:   2019-03-06 11:18:00
featured_image: rails.png
tags: [Web development]
---
First, update the system
```
sudo apt-get update
```

After, install the **build-essential package**
```
sudo apt-get install build-essential
```

<!--more-->

And also **curl.**

```
sudo apt-get install curl
```

Then, we need install **rvm** but first install GPG Keys.
```
gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB
```

Install **RVM** development version.
```
\curl -sSL https://get.rvm.io | bash -s stable
```

After installation run the following command to the rvm works.
```
source ~/.rvm/scripts/rvm
```

Also, for RVM to work properly, you have to check the ***Run command as login shell*** in the terminal.

![Run command as login shell](https://cdn-images-1.medium.com/max/800/1*emo6wiTAV5x632dYxrT7VA.jpeg)

### RVM commands:

```
rvm # show all commands of rvm
```

Install **ruby** interpreter.
```
rvm install 2.5.3 
```
Switch to specified **ruby** interpreter.
```
rvm use 2.5.3
```

Set a default version of ruby.
```
rvm use 2.5.3 --default
```

Check the version of ruby.
```
ruby -v
```

### Install **rails.**
```
gem install rails
```

#### Use NVM (Node Version Manager) to install **Node.js** - The JavaScript runtime is required to compile code for the Rails asset pipeline

To **install** or **update** nvm, you can use the install script using cURL:

```
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.34.0/install.sh | bash
```
or Wget:
```
wget -qO- https://raw.githubusercontent.com/creationix/nvm/v0.34.0/install.sh | bash
```

<sub>The script clones the nvm repository to `~/.nvm` and adds the source line to your profile (`~/.bash_profile`, `~/.zshrc`, `~/.profile`, or `~/.bashrc`).</sub>

<sub>**Note:** If the environment variable `$XDG_CONFIG_HOME` is present, it will place the `nvm` files there.</sub>

```sh
export NVM_DIR="${XDG_CONFIG_HOME/:-$HOME/.}nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm
```

Install node.js

```
nvm install node # "node" is an alias for the latest version
```

To install a specific version of node:
```
nvm install 6.14.4 # or 10.10.0, 8.9.1, etc
```

### Creating a New Rails Project
```
rails new app
```

![Rails new app](https://cdn-images-1.medium.com/max/800/1*FBGD40tAi6tm719N6tPOkg.png)

```
cd app/
rails s # Start server
```

Then, open a browser window and navigate to http://localhost:3000. Yay!

![localhost:3000](https://cdn-images-1.medium.com/max/800/1*cfyIRUPrmf_mrXOS-_qJWg.png)

### References
- [Getting Started with Rails](http://guides.rubyonrails.org/getting_started.html)
- [Node Version Manager](https://github.com/creationix/nvm)
- [rvm-integration/gnome-terminal](https://rvm.io/integration/gnome-terminal)
