#Useful *nix Commands  
This is a list to get comfortable with the command line and some of what it can do. Most of these commands have many more options, and are more powerful than the simple examples here. They are commands I've found useful, but it is by no means an exhaustive list. 
In this repo there is also an IPython Notebook with examples that can be viewed [here](http://nbviewer.ipython.org/github/andrewquitadamo/shell_intro/blob/master/intro_to_shell.ipynb).
There is also a video [here](https://www.youtube.com/watch?v=vt9PtyKktxA).
 
##Moving Around   
###pwd  
Prints path of current directory:  
```
pwd
```
###ls  
List contents of current directory:  
```
ls
```  
List contents of current directory and size:  
```
ls -s
```  
List contents of current directory with permissions, size, and date modified:  
```
ls -l
```  
List  contents of current directory sorted by date modified:  
```
ls -t
```
###mkdir
Creates new directory  
```
mkdir directory_name
```
###cd
Change directory:  
```
cd directory_name
```  
Move one directory up:  
```
cd ..
```  
Move to home directory:  
```
cd
```  
##Moving Files  
###mv  
Move file to another directory:  
```
mv filename directory
```  
Rename file:  
```
mv original_filename new_filename
```  
###cp  
Copy file to another directory:  
```
cp file directory
```  
###rm  
Remove file:  
```
rm file
```  
Remove directory:  
```
rm -r directory
```  
##Working with Files
###touch
Create new file:  
```
touch file
```  
###cat  
Display contents of file:  
```
cat file
```  
Concatenate files:  
```
cat file1 file2 > file3
```  
###head  
Display first 10 lines of a file:  
```
head file
```  
Display first n lines of a file:  
```
head -n file
```  
###tail  
Display last 10 lines of a file:  
```
tail file
```  
Display last n lines of a file:  
```
tail -n file
```  
###sed  
Print i-j lines of a file:  
```
sed -n i,jp file
```   
Delete first line of a file:  
```
sed 1d file1 > file2
```  
Delete i-j lines of a file:  
```
sed i,jd file1 > file2
```  
Replace pattern in file:  
```
sed 's/find/replace/g' file1 > file2
```  
###grep  
Display all the instances of a pattern:  
```
grep 'pattern' file
```  
Count the lines that contain a pattern:  
```
grep -c 'pattern' file
```
###sort  
Sort a file by lines:  
```
sort file1 > file2
```  
Sort a file numerically:  
```
sort -n file1 > file2
```  
Sort a file in reverse:  
```
sort -r file1 > file2
```  
###uniq  
Filter out repeated lines:  
```
uniq file1 > file2
```  
###cut
Get second column from a file
```
cut -f 2 file1
```
Get first to fouth columns:
```
cut -f 1-4 file1
```
###vim  
Open a file in vim to edit:  
```
vim file
```  
###emacs
Open a file in emacs to edit:  
```
emacs file
```  
##Working Remotely  
###ssh  
Log into a server:  
```
ssh username@server.address
```  
Example:
```
ssh username@cobra.urc.uncc.edu
```  
###scp  
Download files from a server:  
```
scp username@server.address:/path/to/file /desired/location/on_local_machine
```  
Upload files to a server:  
```
scp /local/path/to/file/ username@server.address:/desired/location
```  
###wget
Download file:  
```
wget ftp://url/path/to/file
```  
Example:
```
wget ftp://hgdownload.cse.ucsc.edu/goldenPath/hg19/chromosomes/chrY.fa.gz
```  
##Miscellaneous  
###tar
Unzip a tar.gz file:  
```
tar xvfz archive_name.tar.gz
```  
Unzip a .gz file:  
```
gunzip archive_name.gz
```  
###chmod
Allow user, group and others to read, write and execute:  
```
chmod 777 file
```  
Allow user to read, write and execute, group and others to read and execute:  
```
chmod 0755 file
```  
###>
Redirects the output of a command to a file. 
###| 
Redirects the output of a command to another command.  
```
head file | tail -1
```  
###man  
Get the manual page for a command:  
```
man command
```  

