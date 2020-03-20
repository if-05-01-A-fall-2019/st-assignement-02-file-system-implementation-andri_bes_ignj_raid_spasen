# File Systems Implementation

## Assignment --- IGNJATOVIC David

<hr>

#### What has to be done, when creating a file foo.txt?

You have to find a new empty Block too start writing.

#### What has to be done, when the file size has to be increased?

You need to find a new empty Blocks and connect them with the last one.

#### What has to be done if a file is read sequentially?

The easiest way is to read from the starting poitn until the end or maybe to read all block seperate.

#### What has to be done if you want to access foo.txt randomly?

You need to find out by reading which block u need to use.

#### What has to be done when the file size decreases?

You need to write for example empty spaces in the file and then conect the other 2 Blocks by reading and writing in the new emoty Block.

#### What has to be done when a file is deleted?

You need to create space for new files. For example u need to wirte empty spaces in the whole file.
