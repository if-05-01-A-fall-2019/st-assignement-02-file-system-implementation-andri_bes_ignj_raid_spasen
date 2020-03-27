# File System Implementation

### What has to be done, when creating a file foo.txt?
I would first of all, search the current directory or in which directory would I create the file. Very important is to manage the permissions of every user for this file.

When creating the file, it has to be linked to the directory.
After this small Procedure I'll start to write the file on the next free block of the disk and in the first allocated block, I'll write down the permissions of the users, name and type of file and the actual file size as metadata.

The permissions of every user, group and other, would I save in the metadata similar to the unix Systems.
The metadata would be saved in the first block of the file.
So if I need the infos like permissions of the users, file size and the location of the file, I don't have to iterate to find the infos in the file.
Because it's at the start of the file.

Unix Systems save the permissions with octal number. And in the Unix-System the octal numbers are saved, so if the system is checking the permissions of a file. He would compare the octal number of the metadata with the octal numbers in the system.
Every octal number has it's own configuration.


### What has to be done, when the file size has to be increased? Especially take care if it needs additional blocks

You have to use the next free block and link it together with the first block.
It's similar to the nodes in a list.
The ney gree blocks are randomly found on the disk, so they have to be linked.
With linked together, I mean every block should know which address has the previous block and the next block.

### What has to be done if a file is read sequentially?
You have to start at the beginning of the file, so no matter how big the file is. You have to iterate from the beginning to the end, if you want to read the whole file.
So you have to know where you want to edit, add, delete something of the file.

### What has to be done if you want to access foo.txt randomly (seek())?
You have to search the block, you want, and read from the found block.
But in order to do that, you have to iterate from the beginning of the file and end, if you found the searched block.

### What has to be done when the file size decreases? Especially take care if it needs fewer blocks
I'll move all data of smaller blocks(blocks with less data then usually), to the first incomplete block. All empty blocks would be free.

### What has to be done when a file is deleted?
The allocated space, have to be free.
Every Connection to the next block have to be dissolved.
So if a new file is coming, you are able to use the new free space.
