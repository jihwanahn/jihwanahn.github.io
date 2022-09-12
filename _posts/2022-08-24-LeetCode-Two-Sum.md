---
layout: post
title:  " LeetCode : 1. Two Sum "
categories: LeetCode
tag: Problem Solving, LeetCode
author: Jihwan Ahn
---
* content
{:toc}

<h2><a href="https://leetcode.com/problems/two-sum/">1. Two Sum</a></h2><h3>Easy</h3><hr><div><p>Given an array of integers <code>nums</code>&nbsp;and an integer <code>target</code>, return <em>indices of the two numbers such that they add up to <code>target</code></em>.</p>

<p>You may assume that each input would have <strong><em>exactly</em> one solution</strong>, and you may not use the <em>same</em> element twice.</p>

<p>You can return the answer in any order.</p>

<p>&nbsp;</p>
<p><strong>Example :</strong></p>
<pre><strong>Input:</strong> nums = [2,7,11,15], target = 9
<strong>Output:</strong> [0,1]
<strong>Explanation:</strong> Because nums[0] + nums[1] == 9, we return [0, 1].
</pre>


### [1] Code (22.08.24)

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

## Reference

* [1. Two Sum](https://leetcode.com/problems/two-sum/)