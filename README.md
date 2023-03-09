# Data_structure_and_algurithum

#sorting a list

def bubble_optimized(A):
    iterator = 0
    for i in range(len(A)):
        for j in range(len(A)-i-1):
            print(j,"this is J")
            iterator += 1
            if A[j] > A[j+1]:
                A[j],A[j+1] = A[j+ 1], A[j]
        print(i," i")
        
    return A, iterator
    
    
A = [1,9,3,2,5,4,6,7,8,10,11,12]
print(bubble_optimized(A))
            
            
            #END......................................................................\
        
        
        
 #CODE
 
 class Node:
    def __init__(self,data):
        self.data = data
        self.next = None
        
               
class LinkedList:
    def traversal(self):
        first = self.head
        while first:
            print(first.data)
            first= first.next
            
    def insert_new_header(self,new_data):
        new_node = Node(new_data)
        new_node.next = self.head 
        self.head = new_node
            
            
    def search(self,x):
        temp = self.head
        while temp is not None:
            if temp.data == x:
                return True
            temp = temp.next 
        else:
            return False 
        
    def delete_node(self,data):
        temp = self.head 
        while temp is not None:
            if temp.data == data:
                break 
            prev = temp 
            temp = temp.next 
        prev.next = temp.next 
        
    def delete_tail(self):
        temp = self.head 
        while temp.next.next is not None:
            temp = temp.next 
        temp.next = None

     
family = LinkedList()
family.head = Node("Bob")
wife = Node("Amy")
first_kid = Node("Mx")
second_kid = Node("jenny")

family.head.next = wife
wife.next = first_kid
first_kid.next = second_kid


family.insert_new_header("sodair")
family.delete_node("Bob")
family.delete_tail()
family.traversal()

                #END .....................................................................................



            
 
