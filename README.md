# Data Structures and Algorithms in C++

This repository contains my daily practice of Data Structures and Algorithms implemented in **C++**.  
The goal is to strengthen problem-solving skills, improve coding efficiency, and prepare for technical interviews.

I regularly solve problems from platforms like LeetCode, GeeksforGeeks, and other coding resources to build strong fundamentals in DSA.


## Topics Covered

- Arrays
- Strings
- Hashing
- Sliding Window
- Recursion
- Backtracking
- Linked List
- Stack
- Queue
- Trees
- Binary Search Tree
- Heap / Priority Queue
- Graphs
- Dynamic Programming
- Greedy Algorithms
- Bit Manipulation


## Repository Structure

Each folder represents a specific topic in Data Structures and Algorithms.

Example structure:

arrays/
strings/
recursion/
dp/
graph/


Each file contains:

- Problem statement reference
- Approach used
- Time complexity
- Space complexity
- Clean and readable C++ implementation


## Example Code Format

```cpp
/*
Problem: Two Sum
Approach: Hash Map
Time Complexity: O(n)
Space Complexity: O(n)
*/

#include <bits/stdc++.h>
using namespace std;

class Solution {
public:
    vector<int> twoSum(vector<int>& nums, int target) {

        unordered_map<int,int> mp;

        for(int i = 0; i < nums.size(); i++){

            int required = target - nums[i];

            if(mp.count(required)){
                return {mp[required], i};
            }

            mp[nums[i]] = i;
        }

        return {};
    }
};
