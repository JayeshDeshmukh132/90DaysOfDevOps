## Process management commands
top - gives dynamic view of running processes
htop - imporved version of top

ps - show process status
    -ef print detailed overview of all processes 
    aux
    **used with | grep <text> to find specific process**

& - added at end of command to run that command/process in background




## File management commands
    ls - list down files in current dir
    -l list file/dir with permissions
    -a include all hidden files too
    -1 list one by one
    -t sort files/folder according to last modified date/time

mv filename foldername - move file to folder
mv filename1 filename2 - change file name

rm filename - remove file
rm -r folder - recursively remove everything inside folder and delete it
    -f forcefully remove

cp file folder - copy file to a folder
cp -r folder1 folder2 

touch filename.txt - create file

cmd > filename - redirect output of the command to file (overwrite current file contents)
cmd >& filename - redirect output of the command to file ( overwrite current file contents and suppresses output in terminal )
cmd > /dev/null  suppress the o/p of cmd
**cmd >> filename - appends the output of command to the file**
cmd &> filename - redirect output as well as command 
    Same as > file 2>&1 


mkdir -p folder_name - create folder

cat filename - display contents of file
    -b include linenumbers

find /path/of/dir -name "pattern- *.log, *.txt"
    -100m flag that specifies larger than specified

**locate <file_name/folder> gives location of file**

tar -cvf file.tar dir (create compressed version of folder)
tar -xvf file.tar  (unzip folder)

## network management commands
ping server_ip/website_name 

ip addr show - shows the ip addresses

netstat -a list all listening and non-listening ports (legacy command new ss)
        -l lists only listening ports
ss -tulnp
    -t tcp
    -u udp
    -l listening ports

    

telnet <hostname> portnumber - checks whether host has specified port open or not

