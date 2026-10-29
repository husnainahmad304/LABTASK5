PART B - INDIVIDUAL PROJECT: Railway Train Management (Lab 4 + Lab 5)

1) REAL-WORLD PROBLEM
   A railway control office keeps a train timetable that changes all the time:
   a new train is added at a particular position, a cancelled train is
   removed, two trains exchange their slots, and the list is sorted by train
   ID or shown in reverse order.

2) WHY A LINKED LIST IS SUITABLE
   - The number of trains is not fixed; the list grows and shrinks at runtime.
   - Inserting or removing a train in the middle needs no shifting of other
     elements (an array would have to shift every later element).
   - Only the "next" pointers around that position change.
   - Memory is allocated only for trains that really exist.

3) NODE STRUCTURE (self-referential)
   struct TrainNode { int trainID; string trainName; string destination;
                      int priority; TrainNode* next; };
   "next" points to another TrainNode, so trains link into a chain.
   The same node is used by the Priority Queue (Lab 4) and the Linked List (Lab 5).

4) CLASSES
   PriorityQueue (Lab 4): Add, Remove, IsEmpty, IsNotEmpty, PrintQueue
   LinkedList    (Lab 5): Insert, Remove, InsertAt, RemoveAt, Swap, Sort,
                          Reverse, Print, IsEmpty, IsNotEmpty

5) DEMONSTRATION
   Main Menu -> 2 (Train Timetable) -> option 10 loads sample trains,
   then try the other options.

COMPILE (run inside this folder):
   g++ main.cpp Input.cpp TrainNode.cpp PriorityQueue.cpp LinkedList.cpp -o program
RUN:
   .\program.exe
