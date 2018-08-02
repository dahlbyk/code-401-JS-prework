# 401 Prework - Install Node.js

## Configure Bash
Bash has a **Bash Profile** which is a file that allows you to configure
how your terminal behaves and define your own custom functions. Here's
some confiurations that set your default text editor and make it easy
for you to edit your profile in the future.

1. run the command `touch ~/.bashrc ~/.bash_profile`  
   this will make sure the files **~/.bashrc** and **~/.bash_profile** exist  
1. open the `~/.bash_profile` and `~/.bashrc` files in your text editor
1. To ensure `.bashrc` loads when the profile loads, and set your default editor to VSCode, add the following lines to
   the end of your **~/.bash_profile**

``` bash
# Read $HOME/.bashrc, if present.
if [ -f $HOME/.bashrc ]; then
  source $HOME/.bashrc   
fi
 
# set the default editor to VSCode
export EDITOR=code

```

the bash configuration files are loaded by bash at different times - we edit them both to ensure node will always be setup  
* **~/.bash_profile** is the personal initialization file, executed for login shells
  * on OSX this runs every time you open a new terminal window
  * on Linux this runs every time you login to your computer
* **~/.bashrc** is the individual per-interactive-shell startup file
  * on OSX this runs every time you type the command `bash` 
  * on Linux this runs every time you open a terminal or type the command `bash`
* run `source ~/.bashrc` to load the new configuration (or open a new tab)


## Install NVM & Node

[Node Version Manager](https://github.com/creationix/nvm) is a great tool for... managing Node (surprise!). 

1. Follow the installation instructions in the repo README, under the "Git Install" section.
   * This will create the directory `~/.nvm` and install nvm into it.  
   * run `ls -a ~/` and look for the **.nvm** directory
2. Follow the instructions under the "Usage" section to install Node, and ensure setup is correct. 
   * Open a new terminal tab, and run `node -v` to verify the [latest NodeJS](https://nodejs.org/en/) version is installed. 

