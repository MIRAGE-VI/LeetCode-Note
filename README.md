# LeetCode-Note
This is a note recording the progress I made in LeetCode. 

1. Two Sum
public class Solution {
    public int[] twoSum(int[] nums, int target) {
        Map<Integer, Integer> hm = new HashMap<>();                                         //the format should be HashMap<>()
        for(int i = 0; i < nums.length; i++){
            if(hm.containsKey(target - nums[i]))
            return new int[] {hm.get(target - nums[i]), i};                                 //hash.get(key)
            hm.put(nums[i], i);
        }
        throw new IllegalArgumentException("no result!");                                   //donot forget exception process
    }
}
