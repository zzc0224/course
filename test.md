#include <iostream>
#include <algorithm>
#include <cstdio>
#include <cstring>
#include <queue>
#include <stack>
#include <vector>
using namespace std;
struct node
{
    friend bool operator< (node n1, node n2)
    {
        return n1.priority < n2.priority;
    }
    int priority;
    int value;
};
bool cpm(int a,int b)
{
    return a>b;
}
int main()
{
    vector<int> array;
    for(int i =10;i>=0;i--)array.push_back(i);
    sort(array.begin(),array.end(),cpm);
    for(int i =10;i>=0;i--)cout<<array[i];
	system("pause");
    return 0;
}
