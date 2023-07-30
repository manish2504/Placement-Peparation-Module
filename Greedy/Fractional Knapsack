#include <algorithm>

bool compare(pair<int, int> a, pair<int, int> b)
{
    return (double)a.second/a.first > (double)b.second/b.first;
}

double maximumValue (vector<pair<int, int>>& items, int n, int w)
{
    sort(items.begin(), items.end(), compare);
    double weight = 0, value = 0;
    
    for(int i = 0; i < n; ++i)
    {
        if(weight < w)
        {
            if(weight + items[i].first <= w)
            {
                weight += items[i].first;
                value += items[i].second;
            }
            else
            {
                double rem = w - weight;
                weight = w;
                value += rem/items[i].first * items[i].second; 
                break;
            }
        }
        else
            break;
    }
    
    return value;
}
