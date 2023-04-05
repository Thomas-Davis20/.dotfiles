# My Dotfiles
         These are my dotfile configuration files for different software in Bash.
         ## .vimrc
         This is my custom .vimrc configuration for Vim.
         ## .bashrc
	 This is my custom .bashrc configuration for Bash.

#Linux Setup

This Git repository contains scripts and configuration files to set up a new Linux machine with custom configurations.

#Files

'bin/linux.sh'
This script sets up a new Linux machine with custom configurations by performing the following tasks:

1. Checking that the operating system type is Linux.
2. Creating a .TRASH directory in the user's home directory if it doesn't already exist.
3. Renaming the .vimrc file in the user's home directory to .bup vimrc if it exists, and then redirecting the contents of /etc/vimrc to a new .vimrc file in the user's home directory.
4. Adding the statement source ~/.dotfiles/etc/bashrc custom to the end of the .bashrc file in the user's home directory.

'bin/cleanup.sh'
This script removes the changes made by the linux.sh script by performing the following tasks:

1. Removing the .vimrc file in the user's home directory.
2. Removing the line source ~/.dotfiles/etc/bashrc custom from the .bashrc file in the user's home directory.
3. Removing the '.TRASH' directory in the user's home directory.

'Makefile'
This Makefile has two targets:

1. linux: This target runs the linux.sh script after running the cleanup.sh script to ensure that the system is in a clean state before running the linux.sh script.
2. clean: This target runs the cleanup.sh script to remove any changes made by the linux.sh script.

'.vimrc'
This file contains custom configurations for the Vim text editor.

'.bashrc custom'
This file contains custom configurations for the Bash shell, including adding the ~/.local/bin directory to the PATH environment variable and setting the PS1 prompt.
