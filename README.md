### gitlab-shell: ssh access and repository management

#### Code status

* [![CI](http://ci.gitlab.org/projects/4/status.png?ref=master)](http://ci.gitlab.org/projects/4?ref=master)
* [![Build Status](https://travis-ci.org/gitlabhq/gitlab-shell.png?branch=master)](https://travis-ci.org/gitlabhq/gitlab-shell)
* [![Code Climate](https://codeclimate.com/github/gitlabhq/gitlab-shell.png)](https://codeclimate.com/github/gitlabhq/gitlab-shell)
* [![Coverage Status](https://coveralls.io/repos/gitlabhq/gitlab-shell/badge.png?branch=master)](https://coveralls.io/r/gitlabhq/gitlab-shell)


__Requires ruby 1.9+__

### Getting Started

    #sudo adduser --gecos 'GitLab' git

    # create git user 
    sudo su - git

    # Clone gitlab shell
    git clone https://github.com/advatar/gitlab-shell.git

    cd gitlab-shell

    # switch to right version
    git checkout v1.7.8

    cp config.yml.example config.yml

    # Edit config and replace gitlab_url
    # with something like 'http://domain.com/'
    nano config.yml


### Setup

    ./bin/install


### Check 

    ./bin/check


### Repos:
 

Add repo

    ./bin/gitlab-projects add-project gitlab/gitlab-ci.git

Remove repo 

    ./bin/gitlab-projects rm-project gitlab/gitlab-ci.git

Import repo 

    ./bin/gitlab-projects import-project randx/six.git https://github.com/randx/six.git

Fork repo

    ./bin/gitlab-projects fork-project gitlab/gitlab-ci.git randx

Update HEAD

    ./bin/gitlab-projects update-head gitlab/gitlab-ci.git 3-2-stable

Create branch

    ./bin/gitlab-projects create-branch gitlab/gitlab-ci.git 3-2-stable master

Remove branch

    ./bin/gitlab-projects rm-branch gitlab/gitlab-ci.git 3-0-stable

Create tag

    ./bin/gitlab-projects create-tag gitlab/gitlab-ci.git v3.0.0 3-0-stable 

Remove tag

    ./bin/gitlab-projects rm-tag gitlab/gitlab-ci.git v3.0.0


### Keys: 


Add key

    ./bin/gitlab-keys add-key key-782 "ssh-rsa AAAAx321..."

Remove key

    ./bin/gitlab-keys rm-key key-23 "ssh-rsa AAAAx321..."

Remove all keys from authorized_keys file

    ./bin/gitlab-keys clear

