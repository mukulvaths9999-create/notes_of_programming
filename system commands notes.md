# ***linux commands***

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
  
## removing a file
  -> __rm "file one"__  
## i node number
  -> __ls -li__  
  __combining the i node and showing all__  
  -> __ls -lia__    
  -> hard link means that the same i node number is there in direcoty and its sub directory 
## ***whoami*** to ask your name!! 
## reading inside file 
  -> __less <filename>__ you can read inside the file, press q for exit 
## get to know type of file 
  -> file <filename > 
## timestamp 
  
  
