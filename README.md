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

