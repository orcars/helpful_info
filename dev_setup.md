
# Setting up developement environment
## Install RVM and Ruby 
    sudo apt-get update
    sudo apt-get install curl
    \curl -sSL https://get.rvm.io | bash
    gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB
    rvm get stable
    rvm install 2.5.1
    rvm alias create default 2.5.1

## Install Atom
Atom can be downloaded as .deb package from internet and installed using the below command

    sudo dpkg -i <pathtofile> (i.e., ./Downloads/atom-amd64.deb)
or use the below commands to install it from the terminal

    sudo add-apt-repository ppa:webupd8team/atom
    sudo apt-get update
    sudo apt-get install atom
## Update bashrc for RVM
Open new terminal and run the below command

    atom ~/.bashrc

Add the below line in the .bashrc and save it

    [[ -s "$HOME/.rvm/scripts/rvm" ]] && . "$HOME/.rvm/scripts/rvm"

Close the terminal and open a new terminal and run the below command to check whether ruby is installed

    ruby -v
Above command should output the ruby verson. In our case it is 2.5.1

## Install Rails
    gem install rails
    sudo apt-get nodejs
Close the terminal and open a new terminal and run the below command to check whether ruby is installed

    rails -v
Above command should output the ruby verson
## Create Sample app
    mkdir Project
    cd Project
    rails new sample
    cd sample
    rails s

Open browser and access the below url

    http://localhost:3000
