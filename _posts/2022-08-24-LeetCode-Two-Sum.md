---
layout: post
title:  " LeetCode : 1. Two Sum "
categories: LeetCode
tag: LeetCode
author: Jihwan Ahn
---
* content
{:toc}

## Problem URL : **[1. Two Sum](https://leetcode.com/problems/two-sum/)**

### [1] Answer Code (22.08.24)

``` cpp
// Time: 348 ms (37.54%)
// Space: 10.3 MB (75.73%)
class Solution {
public:
    vector<int> twoSum(vector<int>& nums, int target) {
        vector<int> answer (2);
        
        unsigned int length = nums.size();
        for(int i = 0 ; i < length; i++)
        {
            unsigned int left = nums.at(i);
            for(int j = i+1 ; j < length; j++)
            {
                if((left + nums[j]) == target)
                {
                    answer[0] = i;
                    answer[1] = j;
                }
            }                
        }
        return answer;
    }
};
```

---
> Review

* Just normal
