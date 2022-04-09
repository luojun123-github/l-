# l-
二分查找法


#include <iostream>
using namespace std;

class Solution 
{
public:
    int search(vector<int>& nums, int target) 
    {
        int high = nums.size() - 1;
        int low = 0;
        int mid = 0;

        while(low <= high)
        {
            mid = (low+high)/2;
            if(nums[mid] == target)
            {
                return mid;
            }
            else if(nums[mid] > target)
            {
                high = mid - 1;
            }
            else if(nums[mid] < target)
            {
                low = mid + 1;
            }
        }
    
        return -1;
    }
};
