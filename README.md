# File-Compression

Huffman Algorithm is an efficient way for file Compression and Decompression. This program exactly follows huffman algorithm. It reads frequent characters from input file and replaces them with shorter binary codeword. The original file can be produced again without losing any bit.

# Algorithm

1. (Pass 1) Read input file
2. Create sorted linked list of characters from file, as per character frequency
````
for eah character ch from file
 if( ch available in linked list at node p) then 
 {
 	p.freq++;
 	sort Linked list as per node's freq;
 }
 else
 	add new node at beginning of linked list with frequency=1;
````
4. Construct huffman tree from linked list 0. Create new node q, join two least freq nodes to its left and right 0. Insert created node q into ascending list 0. Repeat i & ii till only one node remains, i.e, ROOT of h-tree 0. Traverse tree in preorder mark each node with its codeword. simultaneously Recreate linked list of leaf nodes.
5. Write Mapping Table(character to codeword) to output file.
6. (Pass 2) Read input file.
7. Write codeword in place of each character in input file to output file for each character ch from input file write corresponding codeword into o/p file (lookup in mapping table OR linked list)
8. End
