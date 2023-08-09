#include <stack>

class BSTiterator
{
    stack<TreeNode<int>*> stk;
public:
    BSTiterator(TreeNode<int> *root)
    {
        // write your code here
        pushAll(root);
    }

    int next()
    {
        // write your code here
        TreeNode<int> *temp = stk.top();
        stk.pop();
        pushAll(temp -> right);
        return temp -> data;
    }

    bool hasNext()
    {
        // write your code here
        return !stk.empty();
    }
    
    void pushAll(TreeNode<int>* root)
    {
        while(root != NULL)
        {
            stk.push(root);
            root = root -> left;
        }
    }
};
