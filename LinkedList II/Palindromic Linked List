LinkedListNode<int>* reverse(LinkedListNode<int> *head);

bool isPalindrome(LinkedListNode<int> *head) {
    // Write your code here.
    
    if(head == NULL || head -> next == NULL)
        return true;
    
    LinkedListNode<int> *slow = head, *fast = head;
    
    while(fast -> next != NULL && fast -> next -> next != NULL)
    {
        slow = slow -> next;
        fast = fast -> next -> next;
    }
    
    slow -> next = reverse(slow -> next);
    slow = slow -> next;
    fast = head;
    
    while(slow != NULL)
    {
        if(fast -> data != slow -> data)
            return false;
        fast = fast -> next;
        slow = slow -> next;
    }
    
    return true;
}

LinkedListNode<int>* reverse(LinkedListNode<int> *head)
{
    LinkedListNode<int> *prev = NULL, *next = NULL;
    
    while(head != NULL)
    {
        next = head -> next;
        head -> next = prev;
        prev = head;
        head = next;
    }
    
    return prev;
}
