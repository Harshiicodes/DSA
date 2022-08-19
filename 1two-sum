https://leetcode.com/problems/two-sum/

should not be sorted, since we need to tell the index of elements and sorting it will mess it up (thus no 2-pointer approach)

bruteforce-- 1. pick every element and add it to every other element in array 
2.check if sum is equal to target , if not move on.

vector<int>res;
for(int i=0;i<size-1;i++)
{
for(int j=i+1;j<size;j++){
 if(nums[i]+nums[j]==target){
 res.push_back(i)
 res.push_back(j)
 return res;
 }}}
 return res;
 
 optimized-- 1.use map to store array element with corresponding index
 2.now traverse array and check if diff(target-nums[i]) is present and should not be same as array element
 
 
 vector<int> answer;
        unordered_map<int,int> map;
        for(int i=0;i<nums.size();i++)
            map[nums[i]] = i;
        
        for(int i=0;i<nums.size();i++){
            if(map.find(target-nums[i])!=map.end()&& map[target-nums[i]] != i){  (second condition edge case- Input[3,2,4] target=6  Output [0,0] Expected [1,2])
                answer.push_back(i);
                answer.push_back(map[target-nums[i]]);
                
                
                return answer;
            }
            
        }
        return answer;
