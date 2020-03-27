# File Systems Implementation

## Own Approach

### Required Tasks

* What has to be done, when creating a file foo.txt?
  first we need a new block which we then override. Using the command WriteBlock().

* What has to be done, when the file size has to be increased? Especially take care if it needs    additional blocks
  we find first a empty block which we than add to our existing block. It is important to conect the blocks.

* What has to be done if a file is read sequentially?
  the Command ReadBlock() reads the blocks. You just have to run it for the whole file so it can read all the Blocks

* What has to be done if you want to access foo.txt randomly (seek())?
  choose the blocks you need to read the use ReadBlock()

* What has to be done when the file size decreases? Especially take care if it needs fewer blocks
we can not delete blocks so we just have to override them using ReadBlock() and write empty space in it. 
