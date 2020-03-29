# Remarks of Andricic

* How knows the systems where your file is saved?
  Do you use something like a pointer to it from the directory?
  Which information has the metadata at the start of your file?

* Would you change only the file size information in the metadata or is there more to change?
How do you handle permissions of the users, nobody wants that someone can change the files of your OS?

* Note: If you read a file sequentially, there is no other way to skip a block.
  You have to read every block seperate in the order how its connected.

* I would do it the same way. Maybe with a idea, I would overthink it, because of performance issues with this method. And if you want to start with a movie in the middle, you have to read every block from the beginning to the middle.

* Why would you fill a memory block with not important data or pointless data?
  You are wasting ressources with this method.

* You are not committed to overwrite the content.
  You should only dissolve all Connections and overwrite the metadata.
  The content would be overwritten on the next reservation and the blocks would be never connected in order to read the old data of the previous file.
