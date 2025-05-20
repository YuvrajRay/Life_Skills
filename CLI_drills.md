# CLI Drills

## Practice drill 1

* mkdir hello : create a directory "hello"
* cd hello : navigating to "hello" directory
* mkdir five : create a directory "five"
* cd five : navigating to "five" directory
* mkdir six : create a directory "six"
* cd six : navigating to "six" directory
* touch c.txt : creating a text file named "c.txt"
* mkdir seven : create a directory "seven"
* cd seven : navigating to "seven" directory
* touch error.log : creating a log file names "error.log"
* cd .. : navigating back
* cd .. : navigating back
* cd .. : navigating back
* mkdir one : creating a directory "one"
* cd one : navigating to directory "one"
* touch a.txt : creating a text file named "a.txt"
* touch b.txt : creating a text file named "b.txt"
* mkdir two : creating a directory named "two"
* cd two : navigating to "two" directory
* touch d.txt : crearting a text file named "d.txt"
* mkdir three : creating a directory named "three"
* cd three : navigating to "three" directory
* touch e.txt : creating a text file "e.txt"
* mkdir four : creating a directory named "four"
* touch access.log : creating a log file named "access.log"
* cd .. : navigating back
* cd .. : navigating back
* cd .. : navigating back
* cd .. : navigating back
* find . -name "*.log" -type f : listing down all the files with extension ".log" in the current 
* find . -iname "*.log" : used for character insensitive search
* directory.
* find . -name "*.log" -type f -delete : deleting all the files with extension ".log" in the current directory.
* cd one : navigating to "one" directory
* nano a.txt : opening "a.txt" in nano(a cli based text editor)
* cat a.txt : reading the contents of "a.txt"
* cd .. : navigating back
* rm -R five : removing directory "five" recursively i.e. deleting all sub-folders and sub-files.
* mv one uno : renaming directory "one" to "uno"
* cd uno : navigating to directory "uno"
* mv a.txt two : moving file "a.txt" into directory two.


## Practice drill 2

* wget -O desired_file_name.txt url : download a file from url and give it a name
* head -n 3 'Harry Potter and the Goblet of Fire.txt' - print top 3 lines of the file
* tail -n 10 'Harry Potter and the Goblet of Fire.txt' - print last 10 lines of the file
* grep -io "Harry" 'Harry Potter and the Goblet of Fire.txt' | wc -l 
 - find all harry in the file and count them
* grep -io "Ron" 'Harry Potter and the Goblet of Fire.txt' | wc -l 
 - find all Ron in the file and count them
* grep -io "Hermione" 'Harry Potter and the Goblet of Fire.txt' | wc -l 
 - find all Hermione in the file and count them
* grep -io "Dumbledore" 'Harry Potter and the Goblet of Fire.txt' | wc -l 
 - find all Dumbledore in the file and count them

* awk 'NR==100, NR==200 {print}' "Harry Potter and the Goblet of Fire.txt" - print from line no 100 till 200 from the file
 
* tr -cs '[:alnum]' '[\n*]' < file.txt | sort | uniq | wc -l : 
  * : tr -cs '[:alnum]' '[\n*]' : translate non-alphabetic characters into newlies (\n) , splitting the text into individual words
  * : < 'file.txt' : reads input from text file
  * : sort : sorts the words alphabetically ( required for uniq to work)
  * : uniq : removes duplicate words
  * : wc -l : counts the number of lines - which equals the number of unique words.
  * : wget -O "desired name" url : download file with desired name

## Processes, ports

* ps -C firefox -o pid,ppid : shows process ID and Parend process ID of firefox
* pkill firefox - To kill firefox
* kill -9 9454 - To kill firefox, and 9454 is the process ID extracted through ps -C firefox -o pid,ppid
* ps -eo pid,ppid,cmd,comm,%cpu --sort=%cpu |head -n 4 : shows top 3 processes by CPU uses and details about the processes.
* ps -eo pid,ppid,cmd,comm,%mem --sort=%mem |head -n 4 : shows top 3 processes by Memory usage uses and details about the processes.
* python3 -m http.server 8000: 8000 is the default server port we may ignore passing 8000 in command
* kill -9 486705 : this will kill the python3 server using the Process ID. Process ID is found using "ps -e | grep python3"
* sudo python3 -m hhtp.server 90 : since port 1 to 1023 are privilage port we need to add "sudo"
* ss -tu : displays all active connections and the corresponding TCP/ UDP ports
* ss -ltnup 'sport = :5432' : displays the process that is listening on port 5432