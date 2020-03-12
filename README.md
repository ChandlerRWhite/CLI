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


