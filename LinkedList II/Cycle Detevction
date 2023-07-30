bool detectCycle(Node *head)
{
    Node *slow = head, *fast = head;
    
    while(slow != NULL && fast != NULL && fast -> next != NULL)
    {
        slow = slow -> next;
        fast = fast -> next -> next;
        
        if(slow == fast)
            return true;
    }
    
    return false;
}
