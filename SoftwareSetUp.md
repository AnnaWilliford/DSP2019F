* Download Git: https://git-scm.com/downloads
* Download Notepad++: https://notepad-plus-plus.org/download/v7.7.1.html
* Download Sublime: https://www.sublimetext.com/3
* Download Anaconda: https://www.anaconda.com/distribution/#download-section

* To add new software to PATH so that it can be called from GitBash, open GitBash window and type:
```
#create .bash_profile
$ notepad .bash_profile

#add Notepad++ to path inside .bash_profile
export PATH=$PATH:"C:\Program Files (x86)\Notepad++" 
#set alias
alias npp=notepad++

#add Anaconda to path:
export PATH=$PATH:"$HOME/Anaconda3/"

#set alias for python
alias python='winpty python.exe'

#save and close .bash_profile

#source .bash_profile for changes to take effect. Run this command from GitBash window:
$ source .bash_profile

#now if you type npp at the command line, notepad++ should open
```
When setting up git:
```
$ git config --global core.editor "notepad++"  #if in PATH

#or
$ git config --global core.editor "'C:\Program Files (x86)\Notepad++\notepad++.exe'"

#or on mac, to add Sublime:
$ git config --global core.editor "/Applications/'Sublime Text.app'/Contents/MacOS/'Sublime Text'"

```
