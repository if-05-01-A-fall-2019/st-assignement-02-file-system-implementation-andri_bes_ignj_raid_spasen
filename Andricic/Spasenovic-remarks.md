#REMARKS

Where are the blocks linked?

How can you move the data of the block with the smaller size to the other block?
What if in the firstblock is not enought space do save the data?

Answer: All Blocks of a file are linked together.
        One Node (Memory-Block) has two pointers, first for the previous node and
        the second is for the next node.
        Except the first and last node, they will have also pointers to the directory.
        So it should be possible to jump from the start to end without iterating the whole file.

        If I delete some data for example in the middle of the file.
        And the Memory-Block is not deleted completely, because there is some data left, I would copy the data from the next to the previous node in order to close the memory-gap.

        I would extend it to the next and give the first block the pointer for the next node.
