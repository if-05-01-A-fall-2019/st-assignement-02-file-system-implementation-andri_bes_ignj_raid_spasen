# Remarks of Andricic

* Do you have any metadata? If yes where do you save this information?

* Would you change any information of your file, expect the content?

* Would you overthink the way you read or would you implement your method to read.

* How do you choose the block? How do you know where the block is?

* Your method is wasting much ressources. You could copy the data and overwrite the pointless memory in the block and stash it together. So you would be able to delete the last memory block and prevent gaps in your memory. It's similar to the memory-leaks in C.
