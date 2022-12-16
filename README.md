# Find-Kth-smallest-element
# This is the program to find kth smallest element in the array in O(log k ) time complexity . using Heap data structure..



#include<iostream>
#include<queue>
using namespace std;

int Findelement(int arr[] ,int n, int k)
{
    priority_queue<int>p;

    for(int i=0;i<n;i++)
    {
        p.push(arr[i]);
        if(p.size()>k)
        p.pop();
    }

    return p.top();

}


int main()
{
    int n;
    cout<<"Enter size of an array : "<<endl;
    cin>>n;
    int arr[n];
    cout<<"Enter array Elements : "<<endl;
    for(int i=0;i<n;i++)
    {
        cin>>arr[i];
    }
    int k;
    cout<<" Enter the index number : "<<endl;
    cin>>k;
    int ele = Findelement(arr,n,k);

    cout<<" The "<<k<<"th smallest element is : "<<ele<<endl;
        return 0 ;
}
