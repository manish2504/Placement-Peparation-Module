Node *firstNode(Node *head)
{
	Node *slow = head, *fast = head;
    
    while(1)
    {
        if(fast == NULL || fast -> next == NULL)
            return NULL;
        
        fast = fast -> next -> next;
        slow = slow -> next;
        
        if(slow == fast)
            break;
    }
    
    slow = head;
    
    while(slow != fast)
    {
        slow = slow -> next;
        fast = fast -> next;
    }
    
    return fast;
}
