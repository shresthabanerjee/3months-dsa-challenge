# 3months-dsa-challenge
Handfull of dsa daily problems as a practice starting from scratch
#include <iostream>
using namespace std;

int main() {
	int n;int arr[100];int num;
	std::cin >> num;
	std::cin >> n;
	for(int i=0;i<n;i++)
	{
	    std::cin >> arr[i];
	}
	int start=0;int end=n-1;int mid;int c;
	while(start<=end)
	{
	    mid=(start+end)/2;
	    if(arr[mid]==num)
	    {
	        c++;
	        
	    }
	    else if(arr[mid]>num)
	    {
	        end=mid-1;
	    }
	    else
	    {
	        start=mid+1;
	    }
	}
	   
	   std::cout << c << std::endl;
	   
	   
	return 0;
}
