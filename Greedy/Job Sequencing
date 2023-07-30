#include <algorithm>

struct info
{
    int profit;
    int deadline;
};

bool compare(info a, info b)
{
    return a.profit > b.profit;
}

void insertJob(vector<int>& time, int deadline, int profit)
{
    for(int i = deadline - 1; i >= 0; --i)
        if(time[i] == -1)
        {
            time[i] = profit;
            break;
        }    
}

int jobScheduling(vector<vector<int>> &jobs)
{
    int n = jobs.size();
    int max = jobs[0][0];
    int sum = 0;
    info job[n];
    
    for(int i = 0; i < n; ++i)
    {
        job[i].profit = jobs[i][1];
        job[i].deadline = jobs[i][0] - 1;
    }
    
    sort(job, job + n, compare);
    
    for(int i = 1; i < n; ++i)
        max = max > jobs[i][0] ? max : jobs[i][0];
 
    vector<int> time(max + 1, -1);
    
    for(int i = 0; i < n; ++i)
    {
        int deadline = job[i].deadline;
        int profit = job[i].profit;
        
        if(time[deadline] == -1)
            time[deadline] = profit;
        else
            insertJob(time, deadline, profit);
    }
    
    for(int i = 0; i < max; ++i)
        if(time[i] != -1)
            sum += time[i];
    
    return sum;   
}
