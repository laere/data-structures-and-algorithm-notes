All Rights Reserved to PluralSight. 

<h2>Node - Node Chain</h2> 
Provides a mechanism to contain a piece of data. Provides a means of connecting it self to other nodes, via an object reference (the Next pointer).

      namespace Nodes {
      
        public class Node {
              public int Value { get; set; }
              public Node Next { get; set; }
        }
        
        class program {
          
          static void Main(string[], args) {
          
            //declare first node
            Node first = new Node { Value = 3 };
            //declare second node
            Node middle = new Node { Value = 5 };
            //chains the first two nodes
            first.Next = middle;
            
            Node last = new Node { Value = 7 };
            //chains the previous connected nodes to the last node
            middle.Next = last;
            
          }
        }
      }

<h2>Linked List</h2>
A single chain of nodes. Head pointer(first node). Tail pointer(last node). Operations(add, remove, find, enumerate). Head/Tail initial value = null.

<h4>Singly Linked list</h4>
Each node has a single link to another node. Works great when you only need forward access to the nodes.
<h4>Doubly Linked list</h4>
Contains two pointers, one to the next node and one to the previous node.
 

      public void AddFirst(LinkedListNode<T> node) {
            //save off the head node
            LinkedListNode<T> temp = Head;
            // Point to head to new node
            Head = node;
            // Insert the rest of the list behind the head
            Head.Next = temp;
            
            Count++;
            
            if (Count == 1) {
            // If list is empty, head and tail should both point
            // to the new node.
                  Tail = Head;
            }
      }


<h2>Stack</h2>
A stack is a collection in which data is added and removed. In a Last In First Out Order (LIFO).
Pushing onto a stack(adding), popping off a stack(removing).
