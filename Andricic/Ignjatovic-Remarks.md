# Remarks by Dave
<hr>
How do you know what block do you need to use if you want to increase the file size? Maybe with a pointer?

Answer: I'm using every block like a node of a double concenated list.
        This means every Memory-Block knows his previous and next node.
        In C, I would be using pointers for the connections.
