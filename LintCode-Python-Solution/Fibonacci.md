##斐波纳契数列
###描述

查找斐波纳契数列中第 N 个数。

所谓的斐波纳契数列是指：

前2个数是 0 和 1 ，第 i 个数是第 i-1 个数和第i-2 个数的和。

斐波纳契数列的前10个数字是：0, 1, 1, 2, 3, 5, 8, 13, 21, 34 ...
 
PS：这个题目的解法很多，还有通项公式的解法，最容易想到的是递归，然后递归的时效似乎往往都是最差的……
 
###测试用例：
输入 1，返回 0

输入 2，返回 1

输入 10，返回 34
 
###思路：
 递归的想法是肯定没错的，但是因为时效不好，所以我们想想其它方案。递归的思想其实是从假定答案->寻找已知->已知条件->回溯，这样的一个过程，是逆序求解，那么如果是顺序求解要怎么样呢？一直计算fibonacci数列的下一个数，直到该数是我们想要的，这样的时间复杂度就为O(n)了，而且容易实现，代码如下：

    fibonacci_list = [0, 1]
    while n > len(fibonacci_list):
        fibonacci_list.append(fibonacci_list[-1] + fibonacci_list[-2])
    return fibonacci_list[n-1]
    
当考虑时效还有更好的算法，感兴趣的同学可以自己了解一下，但是编程不只时效重要，实现也很重要。