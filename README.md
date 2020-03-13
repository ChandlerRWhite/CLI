# CLI
Command Line Interface (CLI) learning.

cd (change directory)
  cd ../../ indicates going back up two directories
  Notice that the "/" on the end ensures that this refers to a directory, not any random file. 
  cd ~ to go to the home folder

ls (list in current directory)
  included -ir to see the code and reverse the order

rmdir (remove directory)
  removes a directory iff there are no files currently in the directory
  
mkdir (make directory)

pushd (push directory)
  pushes a directory to a virual list of directories that may be switched between quickly
popd (pop directory)
  pops a directory from the virtual list of directories that may be switched between quickly

touch (creates a new file)

man (looks at the manual entry for a function)
  type q to quit

apropos (similar to man, but searches the description for information on the searched function)

cp (copies a file/directory)
  cp -r allows copying a directory (and contained files)
  overwrites files that have already been created.

mv (moving files, or, rather, renaming them.)

less (displays text file contents)
  type q to quit
  page up / down with arrow keys. Spacebar and 'w' work too. 

cat (spews the whole filel to the screen wtih no paging or stopping)
  
rm (remove)
  BE CAREFUL WHAT YOU REMOVE. 
  -i prompts for removal confirmation

Pipes and Redirection
  Take a command and change where its input and output goes. 
  | takes the output from the command on the left, and "pipes" it to the command on the right.
  < takes and send the input from the file on the right to the program on the left. 
  > takes the output of the command on the left, and writes it to the file on the right.
  >> takes the output of the command on the left, and appends it to the file on the right.

Wildcard Matching
  Sometimes, you want to do a command to a set of files all at once. The way you do this is to use the * (asterisk) symbol to say "anything." Wherever you put the asterisk, the shell will build a list of all the files that match the non-asterisk part. 

Part III Searching

  find STARTDIR -name WILDCARD -print
  $ cd temp
  $ find . -name "*.txt" -print
  $ cd .. 
  $ find . -name "*.txt" -print | less
  $ cd ..
  $ find . -name "*.txt" -print | less
  
1. First go to temp directory
2. Plain find from there for not too many .txt files. 
  "Hey find, start here (.) then find files named "*.txt" and print them"
3. Next go up one directory and do the same command, but this time I pipe the output to less. THis command could run for awhile, so be patient. 
4. Do this again, but this one could take a really long time. 
  Hit control^-c to abort it. 

cat > somefile.txt
  "close" the file with control^-d

grep searches for different words inside certain files.
e.g. grep old *.txt (find "old" in files ending in .txt, can also pass strings with "old guy" with quotes)
grep -i ignores upper / lower case

man
apropos
  Look through all the help files and find potentially relevant help for you

$ env
  TERM_PROGRAM=Apple_Terminal
  TERM=xterm
  SHELL=/bin/bash 
  OLDPWD=/Users/zed/temp
  USER=zed
  COMMAND_MODE=unix2003 
  PATH=/opt/local/bin:/opt/local/sbin:/usr/bin:/bin:/usr/sbin:/sbin:/usr/local/bin:/usr/X11/bin 
  PWD=/Users/zed/
  LANG=en_US.UTF-8
  PS1=$ 
  SHLVL=1
  HOME=/Users/zed 
  LOGNAME=zed
  _=/usr/bin/env
  $ env | grep zed
  OLDPWD=/Users/zed//temp 
  USER=zed
  PWD=/Users/zed/
  HOME=/Users/zed
  LOGNAME=zed
  $ echo $USER 
  zed
  $ echo $PWD
  /Users/zed/
  $ export TESTING="1 2 3" 
  $ echo $TESTING
  1 2 3
  $ env | grep TESTING
  TESTING=1 2 3
  $

"Your shell has these "hidden variables" that can change how other programs work. In this exercise I first print out my environment, just dumping it to the screen. Then I do it again but pipe it through grep to find only the variables with my username in them. Finally, I set an environment variable TESTING to "1 2 3".
You may not run into this too often, but sometimes to get something configured you have to change these. A good example is the PATH variable, which determines the search order for other commands. Changing your PATH is going to be one of your exercises."

env (environment)

How to change the path
https://kb.iu.edu/d/acar

 $ export TESTING="bada bada bing"
  $ echo $TESTING
  bada bada bing 
  $ unset TESTING
  $ echo $TESTING
  
  $ env | grep TESTING
  $
  
  You can also change an environment variable to something else, as well as unset it so it isn't in your environment at all. You can't set an environment variable to nothing ("") to remove it. You have to use a command.

exit

xargs
sudo
chmod
chown
