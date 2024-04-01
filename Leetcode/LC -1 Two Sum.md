Brute Force: O(n^2)
```java
```java
class Solution {
    public int[] twoSum(int[] nums, int target) {
        for(int i = 0; i < nums.length; i++){
            for(int j = i + 1; j < nums.length; j++){
                if(nums[i] + nums[j] == target)
                    return new int[]{i,j};
            }
        }
        return null;
    }
}
```


```

O(n) Solution:
```
```java
class Solution {

public int[] twoSum(int[] nums, int target) {

Map<Integer, Integer> map = new HashMap<>();

  

for(int i = 0; i<nums.length; i++){

int complement = target - nums[i];

if(map.containsKey(complement)) return new int[]{map.get(complement),i };

else map.put(nums[i], i);

}

return null;

}

}
```