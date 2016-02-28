<h2>Node</h2> 
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
