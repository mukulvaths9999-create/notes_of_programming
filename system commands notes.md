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
  __mv dir1/file1 dir2/__ directly moving files without changing directory , source destination   
  __cp -r mydir mydir2__  copy command does not assume recurssion we have to give -r so that it can work  
  but _mv_ commands assumer recursssion so we dont have to tell explicitly  

  __cp -r level1/* new_direct/__ copying inside content of level1 directory to new_direct   

## links : _make links between files_ 
  __ln -s file1 file2 => ln -l source destination__  (soft link ) 
  __ln file1 file2__ creating without s will give them the same i node number (hard link )    

## file size:
_files if they are less than a block take whole block or take {no block}, they will never take part of a block_ 
__stat znew__ for file size   
__du znew__ for aliean , __du -h znew__ for human   
  __uname -a__ give all comprehnsive system information   
  __free__ or __free -h__ gives more readable form about somethings   
  __cat partitions__ tells about partitions __df__ for more   
  
## -----------------------------------------------------------------------------------  

## command line editor (ed editor )
__echo "line-1 hello world" > test.txt__ --> creates a new file named test.txt (or overwrites it if it already exists) and inserts the  string "line-1 hello world" into it.  
__echo "line-2 this is a new line" >> test.txt__ append a second line to this file without erasing the first  

__cat test.txt__ to see the file  

__ed test.txt__ enterning a interactive shell where you can edit a file line by line  
__q__ to quit the shell   

__P__ TO ACTIVATE THE COMMANDS  
  -> __*1__ for first line  
  -> __*$__ for last line of file   
  -> __*,p__ for all content of the fle   
  -> __*2,3p__ for second and third line  
  -> __*/hello/__ search for the pattern (words) in which line it is  
  -> 
  -> __*1__ first line then __*+__ go to the next line, __*-__ go to the previous line  
  -> __*;p__ you go the end of the buffer, from that line in which you are (printing all lines in between ) 
  -> __*%p__ to see all the line  
  -> __*.__ for current line  
  -> __*!date__ give me the date  
  -> 
  -> _i am adding the line_   

  -> __*4__ setting the fourth.   
  -> __*r !date__ read the date, __*,p__ now i will get all lines and then date at bottom but it is not added at the bottom yet  
  -> now, __*w__ to write date into the file  

-> __.d__ to delete the current line  
-> __*1__ selecting position of line(here 1 ), __*a__ write in next line then __.__ to finish line in next line and then enter.  

-> __*2__ go to the line  (this is the line after first line) 

-> __*s/this/This/__ here s for search /word/replacment word/ 

-> __*2p__ you are printing second line (This is the line after first line) 

->  _you have to write __*w__ after making any change_  

-> __*5,6j__ to join 5th and 6th line with each other   
-> __*m1__ moving the current line on position on 1st (line postion start with 0) __*m0__ for 0th position.   
-> __*u__ undo the change that i have done  
##  __1,$s/\(.*\)/PREFIX \1/__    

__1,$__ for the first to last line ,__(.*__: The dot . matches any character, and the asterisk * matches zero or more of those  characters. Together, entire content of the line.)  

PREFIX :text insert at the beginning of each line,  
_\1: This is a back-reference. It tells ed to take the text that was captured inside the \(...\) in the "Find" section and place it here  ._ 

__3,5s/PREFIX/prefix/__ from third to fifth i am substituting the PREFIX to prefix  

## readlink -f /usr/bin/pico  
-> it is pointing to /usr/bin/nano  

.bashrc _the bash shell code_ _copy it for making any change_ 
## nano editor  
  -> visual 
  nano test.bashrc ( i made a copy earlier by cp command of bashrc-> test.bashrc )  
  -> ctrl + o to overwrite the command press enter and ctl+x to out of file   
  _see notes for all commands and features_   

## vi editor 
_just see the pdf bro it has all the commands_  


