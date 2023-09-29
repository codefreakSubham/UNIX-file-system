UNIX File System
----------------------------------
Designed a simple File System having defined constraints using C++.
Implemented multiple functions such as create a file, list all files, delete the file, read and write the file.




Input 
-----------------------------

* Input is taken through Console.

* Input includes the following commands: 
	- mf file-name filecontents
	- df file-name
	- rf file-name1 file-name2
        - pf file-name 
        - ls
	
Commands
-----------------------------

* mf file-name filecontents
	* first check for the uniqueness of the filename
	* create a unique inode for file
	* insert filename and corresponding inode into the meta data.
	* insert the inode and filename into the sets for checking the uniqueness further.
	* calculate the number of disk files required and create disk block files with inodeno_blockno

* df file-name
	* check if the file with given name is present in the file system
	* get the inode of the file to be deleted
	* remove the file entry from the meta data
	* retrieve the number of disk files created for the file to be deleted
	* remove the disk block entry from the file
	* delete all the disk files.
	* remove the file from the list of files
	* remove the inode from the inode list.

* rf file-name1 file-name2
	* check whether the new filename is unique
	* check if the file with given name is present in the file system
	* rename the filename in the metadata
	* remove the file from the list of files
	* insert the new filename into the list of files

* pf file-name 
	* check if the file with given name is present in the file system
	* get the inode of the file to be displayed
	* retrieve the number of disk files created for the file to be displayed
	* display all the disk file contents


* ls
	* list all the files from the meta_data
  
 
 
 ---------------------------------------------------------------
