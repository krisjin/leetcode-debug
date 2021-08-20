### 整数反转

难度: 简单

**题目描述**  

给出一个 32 位的有符号整数，你需要将这个整数中每位上的数字进行反转。

**示例 1:**

输入: 123
输出: 321

**示例 2:**

输入: -123
输出: -321

**示例 3:**

输入: 120
输出: 21

**注意:**

假设我们的环境只能存储得下 32 位的有符号整数，则其数值范围为 [−231,  231 − 1]。请根据这个假设，如果反转后整数溢出那么就返回 0。



### 代码



```java
    public int reverse(int x) {
        int res = 0;
        while (x != 0) {
            // 每一次都在原来结果的基础上变大10倍，再加上余数 x%10，总是会获取最后一个数
            res = res * 10 + x % 10;
            //对x不停除10
            x = x / 10;
        }
        if (res < Integer.MIN_VALUE || res > Integer.MAX_VALUE) return 0;
        return res;
    
```







### 总结



### 参考资料
https://leetcode-cn.com/problems/reverse-integer/

