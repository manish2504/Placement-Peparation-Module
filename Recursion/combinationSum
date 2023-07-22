#include <algorithm>

void getSubset(vector<int>& arr, int i, int sum, int target, vector<int>& sub, vector<vector<int>>& ans);

vector<vector<int>> combinationSum2(vector<int> &arr, int n, int target)
{
	vector<vector<int>> ans;
    vector<int> sub;
    sort(arr.begin(), arr.end());    
    getSubset(arr, 0, 0, target, sub, ans);
    return ans;
}

void getSubset(vector<int>& arr, int i, int sum, int target, vector<int>& sub, vector<vector<int>>& ans)
{
    if(sum == target)
    {
        ans.push_back(sub);
        return;
    }
    
    for(int j = i; j < arr.size(); ++j)
    {
        if(i != j && arr[j] == arr[j - 1])
            continue;
        
        if(sum + arr[j] > target)
            break;
        
        sum += arr[j];
        
        sub.push_back(arr[j]);
        getSubset(arr, j + 1, sum, target, sub, ans);
        sub.pop_back();
        sum -= arr[j];
    }
}
