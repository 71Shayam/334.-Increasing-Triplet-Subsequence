
334. Increasing Triplet Subsequence
- - - - - - - - - - - - - - - - - -
SOLUTION : 

class Solution {
public:
    bool increasingTriplet(vector<int>& nums) {
         if (nums.size() < 3) {
            return false;
        }
        int first_small = INT_MAX;
        int second_small = INT_MAX;
        for (int num : nums) {
            if (num <= first_small) {
               first_small= num;
            } else if (num <= second_small) {
                second_small = num;
            } else {
                return true;
            }
        }
        return false;
    }
};
