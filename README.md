# 3months-dsa-challenge
Handfull of dsa daily problems as a practice starting from scratch
#include <iostream>
using namespace std;
//searching element in nearly sorted array
int main() {
int n;int nums[100]; int target;
std::cin >> n;
std::cin >> target;
for(int i=0;i<n;i++)
{ std::cin >> nums[i];
    
}
int start=0;int end=n-1;int mid;
while(start<=end)
{
    mid=start+(end-start)/2;
    if( nums[mid]==target)
    {std::cout << mid << std::endl; 
    break;}
    if((nums[mid+1]==target)&& (mid+1<=end)){ //if mid=end, mid+1 will b array index out of bound
     std::cout << mid+1 << std::endl; 
     break;}
     if(( nums[mid-1]==target)&&(mid-1>=start)){//if mid=start, mid-1 will b array index out of bound
     std::cout << mid-1 << std::endl; 
     break;}
     if(nums[mid]>=target)
     end=mid-2;
     if(nums[mid]<=target)
     start=mid+2;
     

}

	return -1;
}
