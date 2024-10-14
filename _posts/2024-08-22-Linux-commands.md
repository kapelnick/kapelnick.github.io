# Linux commands and shell scripting

*notes on the course "Linux commands and shell scripting by IBM"

Shell is powerful *user interface* (GNU Bourne-again shell)

Interactive and scripting language that can be used to automate tasks

Other shells include *sh, ksh, tcsh, zsh* and *fish*

`printenv SHELL` 
returns the path to the default shell program

To enter bash simply type
	bash

	whoami 
returns user username

	id
returns current user ID and group ID

`id -u` returns numerical id

`id -u -n` returns the name of the user

`uname`
returns operating system name (kernel, version)

`uname -s -r` returns the name and version of the system

`uname -v` returns detailed information

`ps` returns the running process and IDs

`ps -e` lists all processes running on the system

`top` short for *table of processes*, returns resource usage

example: `top -n 3` displays the top 3 processes
 
`df` returns mounted filesystems

`df -h` shows all filesystems

`df -h ~` returns the table for the */home* directory, while *-h* makes the output human readable

`man` returns the reference manual for any command 

`date` returns the current time and date

## working with files

`cp` to copy a file

`mv` to move a file

`rm` to remove file

`touch` creates an empty file or updates the timestamp

`chmod` change file permissions

`wc` gets the count of lines, words, and chars, in a file

`grep` returns lines in file matching pattern

## navigating working with directories

`ls` list files and directories

`find` finds files in working directory tree

`pwd` get present working directory

`mkdir` make new directory

`cd` change directory

`rmdir` removes an entire directory

## printing file and string contents

`cat` print file contents

`more` print file contents page by page

`head` print first *N* lines

`tail` print last *N* lines

`print` string or value of a variable


## compression and archiving

`tar` archive a set of files

`compress` compress a set of files

`unzip` extracts files from a compressed directory

## networking

`hostname` print hostname

`ping` sends packets to a URL and prints the response

`ifconfig` display system network interfaces

`curl` displays the contents of a file at a URL

`wget` download file from URL


## informational commands

`echo` to print string or variable

`echo -e "This will be printed \in two lines"` is used when working with special chars

`echo "Hello"` produces `Hello`

`echo $PATH` produces the value of the `PATH` variable

`date` displays the current date and time

`man` displays the manual for each command

`man -k .` lists all commands on the system

### TLDR 
TLDR Pages, short for "Too Long; Didn't Read" and also known simply as *tldr*, provide examples for common use cases of various commands. The format of TLDR pages is similar to that of a cheat sheet.

install using `npm install -g tldr`

## file and directory navigation commands

`ls Downloads` list files within the target directory

`ls -l` shows child files and directories, permissions, owners, last modified

`ls -R`

`pwd` print working directory

`cd ..` to change to the parent directory

`cd ~` absolute path to */home* directory

`find . -name "a.txt"` case sensitive search only the current directory for a file named *a.txt*

## file and directory management commands

`mkdir test` makes a new directory named *test*

`rm file1` removes the file named *file1*

`rm -r folder1` deletes the entire directory

The `rm` command is used to delete files, ideally with the `-i` option, which creates a prompt to ask for confirmation before every deletion.

`rmdir` only deletes **empty** directories

`touch a.txt b.txt c.txt` creates three empty files

`cp` copy a file or directory

`cp /source/file /destination/filename` to copy the file from source to destination providing a new filename

`cp /source/file /deistination/` to simply copy the file

`cp -r /source/dir/ /dest/dir/` to copy the entire directory to a new destination dir

`mv /source/file /dest/dir/` moves a file

`mv /source/dir /dest/dir/` moves an entire directory
 
### file permissions

`chmod +x myscript.sh` gives execution rights to the script

`-rw` denotes rights to read and write

`ls -l` prints permissions of files

![[Pasted image 20240501151410.png]]

>	`$ echo "Who can read this file?" > my_new_file`
>	`$ more my_new_file`
>	`Who can read this file?`
>	`$ ls -l my_new_file`
>	`-rw-r--r-- 1 theia users 25 Dec 22 17:47 x`


![[Pasted image 20240501151131.png]]

>	`chmod go-r my_new_file`
>	`ls -l my_new_file`
>	`-rw------- 1 theia users 24 Dec 22 18:49 my_new_file`

In the `chmod` command, `go-r` is the permission change to be applied, which in this case means removing for the group (`g`) and others (`o`) the read (`r`) permission. The `chmod` command can be used with both files and directories.

## viewing file content

`cat` for catenate prints the entire file contents

`more` prints content in a page-by-page format

`head` prints first 10 lines

`tail` prints last 10 lines

`wc` counts words, lines, characters (including /n)

use `-l` for lines, `-c` for characters and `-w` for words

## wrangling text files

`sort filename.txt` sort A-Z

`sort -r filename.txt` sorts Z-A

`uniq filename.txt` filters out the repeated **consecutive** lines

`grep` stands for *global regular expression print* and returns a line matching a pattern

example `grep ch filename.txt` finds lines having `ch` chars

`grep -i ch filename.txt` for case insensitive search of `ch`

`cut` extracts a section from each line

`cut -c 2-9 filename.txt` cuts between the range from each line

`cut -d ' ' -f2 filename.txt` cuts the second field `f2`, delimited by empty space `' '`

`paste filename2.txt filename3.txt` merge lines from different lines. Note that `paste` uses **tab** as a default delimiter

`paste -d "," filename1.txt filename2.txt` uses *,* as delimiter


## networking

`hostname -i` returns the IP address of the machine

`ifconfig` stands for interface configuration

`ifconfig eth0` to see information about a specific device

`ping URL` sends ICMP packets to a target URL

`curl` is a client URL used to transfer data to and from a URL

`curl ww.google.com -o google.txt`

`wget` used to retrieve files at a given URL

`wget URL/filename.txt`

## file archiving and compression

`tar` for *tape archiver* used to archive file or directories to a **tarball**

`tar -cf filename.tar dir` is used to make a new archive file `filename.tar` using a provided folder or file `dir`

`tar -czf filename.tar.gz dir` using the GNOME compression program **g-zip**

`tar -tf notes.tar` lists archive contents

`tar -xf filename.tar dir` used to extract archive contents

`tar -xzf filename.tar.gz dir` to decompress and unpack an archive

`zip` compress files and directories to an archive

>	zip: compress --> archive
>	tar: archive --> compress

`zip -r filename.zip dir`

`unzip filename.zip` to unpack and decompress a zipped archive

### Summary

>- A shell is an interactive user interface. You use shell commands to navigate and work with files and directories.
- The _**curl**_ and _**wget**_ commands display and download files from URLs, and the _**cat**_ and _**tail**_ commands display file contents.
- You can get user information with the _**whoami**_ and _**id**_ commands, and get operating system information using the _**uname**_ command. You can check system disk usage using the _**df**_ command and monitor processes and resource usage with _**ps**_ and _**top**_. Print string or variable value using _**echo**_, print and extract information about the date with the _**date**_ command, and read the manual for any command using _**man**_.
- _**ls**_ lists all files and directories within a specified directory tree and _**cd**_ navigates between directories. The _**find**_ command finds files in your directories.
- Relative paths are relative to your current working directory, while absolute paths stand independently
- You can create files and directories with the _**touch**_ and _**mkdir**_ commands, delete them with _**rm**_ and _**rmdir**_, and copy and move them _**cp**_ and _**mv**_.
- The _**cat**_, _**more**_, _**head**_, and _**tail**_ commands allow you to sort and view file contents or view only a certain number of lines. Determine line, word, and character counts with _**wc**_.
- You can use _**sort**_ to view the lines of a file alphanumerically and _**uniq**_ to remove repeated lines from your view. _**grep**_ gets the lines of a file that match your desired criteria, and _**cut**_ extracts slices and fields from lines. You can merge lines from different files using _**paste**_.
- _**hostname**_ and _**ifconfig**_ allow you to view the network configuration. You can test a network connection using **_ping_** and send and receive data using _**curl**_ and _**wget**_.
- Compression preserves storage space, speeds data transfer, and reduces system load.
- _**zip**_ compresses files and folders prior to archiving them. _**tar**_ archives and compresses files and directories into a tarball. _**unzip**_ unpacks and decompresses a zipped archive, and _**tar**_ can also decompress and unpack a tar.gz archive.
