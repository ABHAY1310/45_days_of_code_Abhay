# 45_days_of_code_Abhay
A code everyday keeps the fear away
DAY -1
PROBLEM OF THE DAY-LEETCODE
class Solution {
public:
    bool containsNearbyDuplicate(vector<int>& nums, int k) {
       unordered_map<int,int>mp;
       for(int i=0;i<nums.size();i++){
           if(mp[nums[i]]>0 && abs(i+1-mp[nums[i]])<=k ){
               return true;
           }
           else{
  mp[nums[i]]=i+1;
           }
         
       }
       return false; 
    }
};
