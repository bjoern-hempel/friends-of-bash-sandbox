# Friends of ba$h sandbox

This is an application sandbox that uses the friends of bash framework (https://github.com/bjoern-hempel/friends-of-bash). It contains the first needed scripts including an install script (./install) and the first version of a base main script (bin/run). Adopt it for your own usage.

## Usage

First create an empty repository ([application-name]) with your repository provider of your choice (e.g. github). Then download the application sandbox from here. Afterwards replace [application-name] with the name of your repository:

```
user$ wget https://github.com/bjoern-hempel/friends-of-bash-sandbox/archive/master.zip
user$ unzip master.zip
user$ mv friends-of-bash-sandbox-master [application-name]
user$ cd [application-name]
user$ vi config/config
```

Replace both variables: repositoryName and mainScript (default bin/run)
If you change the mainScript name, don't forget to rename the bin/run application name.

```
user$ git config --global user.name "Your Name"
user$ git config --global user.email "[your@email.com]"
user$ git init
user$ git remote add origin [git@github.com:github-name/application-name.git]
user$ git add .
user$ git commit -m "first version"
user$ git push -u origin master
```

Edit the README.md and LICENSE file. Make your general changes and commit it. Install your application globally:

```
user$ sudo ./install -g
user$ [application-name] --help
```

or install only the friends of bash library locally to use your application directly within your development path:

```
user$ ./install
user$ bin/[main-script] --help
```

Have fun! :)
