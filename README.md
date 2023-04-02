README.md
=========


### Install tool ###

    $ mkdir -p ~/bin
    $ ln -s $(pwd)/build_rpm ~/bin/build_rpm

    Make sure $HOME/bin is in your $PATH


### Tool requirements ###

The tool requires to following to exist in the directory it tries to build:

* kube.yaml
* 3pp/files  (optional if the 3pp directory is missing)

Container reqstrictions:

* User with uid=1000 inside the container

It will also not allow any outgoing network connections so everything required
should be found from the base directory.


### Using the tool to build ###

For the actual build process:

    $ git clone git@github.com:johro81/rush.git
    $ cd rush
    $ build_rpm .
    $ find ./dist

