1. Download Git: https://git-scm.com/downloads
2. Download Notepad++: https://notepad-plus-plus.org/download/v7.7.1.html

3. To add notepad++ to PATH so that it can be called from the command line, open GitBash window and type:
```
#create .bash_profile
$ notepad .bash_profile

#add Notepad++ to path inside .bash_profile
export PATH=$PATH:"C:\Program Files (x86)\Notepad++" 

#set alias
alias npp=notepad++

#save and close .bash_profile

#source .bash_profile for changes to take effect. Run this command from GitBash window:
$ source .bash_profile

#now if you type npp at the command line, notepad++ should open
```
