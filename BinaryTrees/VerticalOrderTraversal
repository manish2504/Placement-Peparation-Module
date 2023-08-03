#include <map>
#include <queue>

vector<int> verticalOrderTraversal(TreeNode<int> *root)
{
    //    Write your code here.
    vector<int> ans;
    map<int, map<int, vector<int>>> nodes;
    queue<pair<TreeNode<int>*, pair<int, int>>> q;
    
    if(root == NULL)
        return ans;
    
    q.push({root, {0, 0}});
    while(!q.empty())
    {
        auto temp = q.front();
        q.pop();
        
        TreeNode<int>* frontNode = temp.first;
        int hd = temp.second.first;
        int lvl = temp.second.second;
        
        nodes[hd][lvl].push_back(frontNode -> data);
        
        if(frontNode -> left)
            q.push({frontNode -> left, {hd - 1, lvl + 1}});
        if(frontNode -> right)
            q.push({frontNode -> right, {hd + 1, lvl + 1}});
    }
    
    for(auto i : nodes)
        for(auto j : i.second)
            for(auto k: j.second)
                ans.push_back(k);
    
    return ans;
}
