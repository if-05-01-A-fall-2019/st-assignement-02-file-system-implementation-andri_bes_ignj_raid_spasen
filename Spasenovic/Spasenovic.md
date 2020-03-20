
#File System Implementation

###What has to be done, when creating a file foo.txt?
When creating a file, first you have to find a new block. Then you have to override it.

###What has to be done, when the file size has to be increased? Especially take care if it needs additional blocks
A new block has to be found. The following block doesn't have to be the next in the System so you have to find it random.
But do not forget to connect the blocks.

###What has to be done if a file is read sequentially?
Read the whole file till the end.

###What has to be done if you want to access foo.txt randomly (seek())?
Read just the blocks you need


###What has to be done when the file size decreases? Especially take care if it needs fewer blocks
You can put in the "deleted" blocks a default value so you can see it's empty

###What has to be done when a file is deleted?
When deleting a file you can write a "0" value in the used blocks so you can see it's empty
