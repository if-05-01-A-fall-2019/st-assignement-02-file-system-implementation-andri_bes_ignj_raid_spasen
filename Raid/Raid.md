#File Systems Implementation

##Own Approach

###Required Tasks

* What has to be done, when creating a file foo.txt?
first we need a new block which we then override it.

* What has to be done, when the file size has to be increased? Especially take care if it needs additional blocks
we find first a empty block which we than add to our existing block. 
