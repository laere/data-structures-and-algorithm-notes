
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

