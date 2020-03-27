# File System Implementation

### What has to be done, when creating a file foo.txt?
I would first of all, search the current directory or in which directory would I create the file. Very important is to manage the permissions of every user for this file. When creating the file, it has to be linked to the directory.After this small Procedure I'll start to write the file on the next free block and in the first allocated block, I'll write down the permissions of the users, name and type of file and

### What has to be done, when the file size has to be increased? Especially take care if it needs additional blocks

You have to use the next free block and link it together with the first block.
It's similar to the nodes in a list.

### What has to be done if a file is read sequentially?
I would try it with Threads. I'm not sure if reading all blocks with seperate Threads, is possible.
Reading every block with seperate Threads, would be more efficient.

### What has to be done if you want to access foo.txt randomly (seek())?
You have to search the block, you want, and read from the found block.

### What has to be done when the file size decreases? Especially take care if it needs fewer blocks
I'll move all data of smaller blocks(blocks with less data then usually), to the first incomplete block. All empty blocks would be free.

### What has to be done when a file is deleted?
The allocated space, have to be free.
Every Connection to the next block have to be dissolved.
So if a new file is coming, you are able to use the new free space.
