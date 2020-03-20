Benjamin Besic 3ahif
# File Systems Implementation

## Tasks
* What has to be done, when creating a file foo.txt?  
  WriteBlock() on the next block that is free has to be executed and has to be
  linked with the directory block

* What has to be done, when the file size has to be increased? Especially take    care if it needs additional blocks  
You choose the next free blocks from the disk and WriteBlock() and then you have
to link these blocks so that the file can be read properly. Maybe writing links.

* What has to be done if a file is read sequentially?
Run ReadBlock() until the file is finished (all blocks of the file are read)

* What has to be done if you want to access foo.txt randomly (seek())?  
ReadBlock() on only the certain parts of the file (blocks) that you need

* What has to be done when the file size decreases? Especially take care if it   needs fewer blocks    
WriteBlock() on the parts that you dont need with empty space and remove links
so that the block is free

* What has to be done when a file is deleted?  
WriteBlock() on the blocks that have to be deleted with empty space to make it free
and overwrite the links.
