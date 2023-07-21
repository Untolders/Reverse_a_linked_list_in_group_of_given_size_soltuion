# Reverse_a_linked_list_in_group_of_given_size_soltuion
Reverse a Linked List in groups of given size solution

//{ Driver Code Starts

#include<bits/stdc++.h>

using namespace std;


struct node

{

    int data;
    
    struct node* next;
    
    
    node(int x){
    
        data = x;
        
        next = NULL;
    
    }
    
};


/* Function to print linked list */

void printList(struct node *node)

{

    while (node != NULL)
    
    {
    
        printf("%d ", node->data);
        
        node = node->next;
    
    }
    
    printf("\n");

}


// } Driver Code Ends

/*

  Reverse a linked list
  
  The input list will have at least one element  
  
  Return the node which points to the head of the new LinkedList
  
  Node is defined as 
  
    struct node
    
    {
    
        int data;
        
        struct node* next;
    
        node(int x){
        
            data = x;
            
            next = NULL;
        
        }
    
    
    }*head;

*/


class Solution

{

    public:
    
    struct node *reverse (struct node *head, int k)
    
    { 
    
         node* prev = NULL;
    
    node* curr = head;
    
    node* temp = NULL;
    
    node* tail = NULL;
    
    node* newHead = NULL;
    
    node* join = NULL;
    
    int t = 0;
 
    // Traverse till the end of the linked list
    
    while (curr) {
    
        t = k;
        
        join = curr;
        
        prev = NULL;
 
        // Reverse group of k nodes of the linked list
        
        while (curr && t--) {
        
            temp = curr->next;
            
            curr->next = prev;
            
            prev = curr;
            
            curr = temp;
        
        }
 
        // Sets the new head of the input list
        
        if (!newHead)
        
            newHead = prev;
 
        /* Tail pointer keeps track of the last node
        of the k-reversed linked list. We join the
        tail pointer with the head of the next
        k-reversed linked list's head */
        
        if (tail)
        
            tail->next = prev;
 
        /* The tail is then updated to the last node
        of the next k-reverse linked list */
        
        tail = join;
    
    }
 
    /* newHead is new head of the input list */
    
    return newHead;

    }

};


//{ Driver Code Starts.

/* Drier program to test above function*/

int main(void)

{

    int t;
    
    cin>>t;
     
    
    while(t--)
    
    {
    
        struct node* head = NULL;
        
        struct node* temp = NULL;
        
        int n;
        
        cin >> n;
         
        
        for(int i=0 ; i<n ; i++)
        
        {
        
            int value;
            
            cin >> value;
            
            if(i == 0)
            
            {
            
                head = new node(value);
                
                temp = head;
            
            }
            
            else
            
            {
            
                temp->next = new node(value);
                
                temp = temp->next;
            
            }
        
        }
        
        
        int k;
        
        cin>>k;
        
        
        Solution ob;
        
        head = ob.reverse(head, k);
        
        printList(head);
    
    }
     
    
    return(0);

}


// } Driver Code Ends
