Create .bash_profile file. In GitBash window type:
```
#create .bash_profile
notepad .bash_profile

#add Notepad++ to path inside .bash_profile
export PATH=$PATH:"C:\Program Files (x86)\Notepad++"  
alias npp=notepad++

#save and close .bash_profile

#source .bash_profile for changes to take effect. Run this command from GitBash window:
source .bash_profile

#now if you type npp at the command line, notepad++ should open
```
