# The Two Sum leetcode problem

The two sum problem is a problem which takes an array and a target and attempts to determine which index values when added together can equal the target number. This problem is meant to test the user's understanding of indexing, loops and algorithmic thinking. The below is solutions I came up with for these problems and the advantages to each solution. 

## Brute force 

The brute force method of solving the two sum leetcode problem specifically focuses on testing every position within the array until we arrive at the positions that equal the target. This method is a great simple way to solve this problem and works well when an array is shorter. 

### High-Level Steps:

1. **Start the Outer Loop**: The outer loop begins at the start of the array and selects the first element (e.g., at index 0) to be the first number in our potential pair.
2. **Start the Inner Loop**: For the number selected by the outer loop, the inner loop begins at the next element in the array. Its job is to pair the outer loop's number with every other number that comes after it.
3. **Check the Current Pair**: Inside the inner loop, add the number from the outer loop and the current number from the inner loop. Check if this sum equals the target.
4. **Handle a Successful Match**: If the sum matches the target, the problem is solved. The two numbers from the current outer and inner loop positions are the answer. The process stops.4.
5. **Continue the Inner Loop**: If the sum does not match the target, the inner loop moves to the next element and repeats the check (Step 3). It continues this until it has checked all subsequent numbers against the outer loop's number.
6. **Advance the Outer Loop**: Once the inner loop finishes without finding a match, the outer loop advances to the next element in the array (e.g., to index 1). This new element becomes the first number for a new set of pairs.
7. **Repeat the Entire Process**: A new inner loop begins again from the element following the new position of the outer loop. This entire process (Steps 2-6) repeats until a match is found.

~~~
#Python Solution
class Solution:
#This defines the class called solution 
    def twoSum(self, nums: List[int], target: int) -> List[int]:
    #The range length function out puts the index specified
    #they are then assigned to the variable x and y
    #The inner loop is a position ahead of the outer loop ensuring the different positions 
            for x in range(len(nums)):
            # Outer Loop       
                for y in range(x+1, len(nums)):
                # Inner Loop
                    sum = nums[x] + nums[y]
                    if sum == target: 
                        return [x,y]
~~~

```mermaid
flowchart TD
    A(Start) --> B[/Get array and target/];
    B --> C[/Step 1: Start the Outer Loop/];
    C --> D[/Step 2: Start the Inner Loop/];
    D --> E{Step 3: Check if the pair's sum equals the target};
    E -- Yes --> F[/Step 4: Success! Return the pair/];
    F --> G(End);
    E -- No --> H{Has the inner loop checked all numbers?};
    H -- No --> D;
    H -- Yes --> I{Has the outer loop checked all numbers?};
    I -- No --> C;
    I -- Yes --> J[No match found];
    J --> G;
```

### Brute Force Big O Calculation

## Hashmap 
The hashmap method of solving the two sum leetcode problem focuses on efficiency as a means of solving this problem. We first initialize the dictionary with the array values as the keys and the array indexes as the values. We find the complement which would be the target value subtracted by the current value to determine one half of the addition that will equal the target. That way we can stop prior to getting to the end of the dictionary once we find the two values that add up to the target. Moreover, the speed of the lookup is much faster because it does not need to iterate through each value it just needs to find the complement. 

### High-Level Steps:

1. **Build the Hashmap**: We first initialize the hashmap 
2. **Iterate array values through hashmap**:
3. **Initiate second loop**: Create complement 
4. **Initiate Search for complement**:
5. **Return Two Sum Indexes**:

~~~
#Python Solution 
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        hashmap = {}
        #initialize Hashmap
        for ind,val in enumerate(nums):
            hashmap[val] = ind
            #Create hashmap and fill values  
        for x,y in enumerate(nums):
            complement = target - y
            #Create complement which would be one of the values in the addition 
            if complement in hashmap:
                if x == hashmap[complement]:
                #Prevent addition between two values in the same index position 
                   continue
                else:
                     return [x, hashmap[complement]]
~~~

```mermaid
flowchart TD

```

### Big O Calculation