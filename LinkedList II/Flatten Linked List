Node* merge(Node *a, Node *b);

Node* flattenLinkedList(Node* head) 
{
	// Write your code here
    if(head == NULL || head -> next == NULL)
            return head;
    
    return merge(head, flattenLinkedList(head -> next));
}

Node* merge(Node *a, Node *b)
{
    Node *result;
    
    if(a == NULL)
        return b;
    if(b == NULL)
        return a;
        
    if(a -> data < b -> data)
    {
        result = a;
        result -> child = merge(a -> child, b);
    }
    else
    {
        result = b;
        result -> child = merge(a, b -> child);
    }
        
    result -> next = NULL;
    return result;
 }
