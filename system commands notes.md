# ***linux commands***
## ps gives a snapshot of current progress 


## cd ->
  __to change the directory__ 
  __***cd ~*** for home directory__
  __***cd -*** for getting in previous directory 
  
## mkdir ->
  __to make a directory__   
  -> eg -> mkdir level1 
  
## chmod g-r level1  
  -> __removed the read permission from the group__  
  -> __+__ to give permission __-__ to remove the permission   
  -> __u__ for user, __g__ for group, __o__ for others    
  -> __r__ for read , __w__ for write and **x** for executable   
  
  ___using code for change___ 
  -> __chmod 700 level1__ ie. only having user permission and removing permission for group and other 
  
## creating files in directory 
  -> __touch file1__ 
  
## ***making copy of a file***
  -> __cp file1 file2__
  
## moving file to one above 
  -> __mv file2 ..__  
  --> using mv to change file name   
    --> __mv file2 file2a__  
  --> moving file inside:  
    --> __mv file2a level1__  
    
## man--> for manual 
  -> eg: man rm   
  
## making an alias so that it ask everytime: 
  -> __alias rm="rm -i"__   
  -> it will ask "y" or "n"  
  __unalias rm__ to remove the rm as an alias

  
## removing a file
  -> __rm "file one"__  
## i node number
  -> __ls -li__  
  __combining the i node and showing all__  
  -> __ls -lia__    
  -> hard link means that the same i node number is there in direcoty and its sub directory   
## ***whoami*** to ask your name!! 
## reading inside file   
  -> __less filename__       
  --> you can read inside the file, press q for exit   
## get to know type of file     
  -> file filename    
  
## timestamp 
## to show inside the sub direcotry   
  -> __ls -l level1__  
## to get long version of directory    
  -> __ls -ld level1__  
  -> __ls -ldi level1__ -> to get the i node number     
  -> __very flexibele__ -> ls -l level1 -di <==> ls -d level1 -li <==> ls -i level1 -dl <==> ls level1 -idl      
  --> also like __ls -l --directory --inode level1__ some has long form some does not, use man command for it     
## knowing files better wali command   
  -> __less profile__ to see content of a file, here profile is name of the file     
  -> __cat profile__  to concatente the file data on screen, it just dump the data     
  --> __more profile__ similar to less   
  -> __head profile__ just print the first 10 lines of a file     
  -> __head -n 5 profile__ print the number of lines you want   
  -> __tail profile__ last ten lines of profile

## more commands    
  -> __wc profile__ give us lines words and bytes of a file 
  -> __wc -l profile__ for just number of  lines 
  -> __which less__ gets to know the location of command 
  -> __whatis which__ gives us a short description of how things are 

## get to know more commands
  -> __apropos__ or __man -k__ get to know new command by keyword 

## shell commands:
  -> __help__ get to know shell and its commands 
  -> __info__ get informaton about commands and then click on star to enter inside to see inside commands 
    -> use __<__ to get one step out 
  -> __type ls__ give us information about a particular command one liner

## setting a shortcut 
  -> __alias ll="ls -l"__ it makes shortcut to command 
  use -> ll 

  -> __alias__ to get to know all alias present 
  -> __unalias ll__ to remover the alias 

## multiple argument 
  -> __touch file1 file2 file3__ three files creating

  __remove a filled directory -> not possible, so either make it empty or__
  use __rm -r mydir__ forced removal of directory 

  -> copying one direcotry to other __
  __cp -r mydir mydir2__ 
  
