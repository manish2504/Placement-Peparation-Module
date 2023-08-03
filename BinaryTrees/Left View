void leftView(TreeNode<int> *root, int level, vector<int>& ans);

vector<int> getLeftView(TreeNode<int> *root)
{
    //    Write your code here
   vector<int> ans;
   leftView(root, 0, ans);  
   
   return ans;
}

void leftView(TreeNode<int> *root, int level, vector<int>& ans)
{
    if(root == NULL)
        return;
        
    if(level == ans.size())
        ans.push_back(root -> data);    
        
    leftView(root -> left, level + 1, ans);
    leftView(root -> right, level + 1, ans);
}
