#include <bits/stdc++.h> 

int next(int left, vector<int>& arr);
int prev(int right, vector<int>& arr);

string fourSum(vector<int>& arr, int target, int n) {
    // Write your code here.
    int left, right;
    int rem;
    
    sort(arr.begin(), arr.end());
    
    for(int i = 0; i < n-3; ++i)
    {
        for(int j = i + 1; j < n-2; ++j)
        {
            rem =  target - arr[i] - arr[j];
            left = j + 1;
            right = n - 1;
        
            while(left < right)
            {
                if(arr[left] + arr[right] == rem)
                    return "Yes";
                else if(arr[left] + arr[right] < rem)
                    left = next(left, arr);
                else
                    right = prev(right, arr);
            }    
        }
    }
    return "No";
}

int next(int left, vector<int>& arr)
{
    int n = arr.size();
    
    for(int i = left + 1; i < n; ++i)
        if(arr[i] != arr[left])
            return i;
}

int prev(int right, vector<int>& arr)
{
    for(int i = right - 1; i > 0; --i)
        if(arr[i] != arr[right])
            return i;
}
