---
layout: post
title: 递归方法，多个单增链表合并为一个单增链表
categories: [算法]
description: 多个递增链表合并
keywords: 链表， Java, 合并链表, 有序链表, 递归
---
# 递归方法，多个单增链表合并为一个单增链表

存在两个或多个在链表内单调递增的链表，需要将其合并成一个仍然单调递增的链表，且不损失任何数据。

## 需要合并的链表结构

```java

public class ListNode {
    int val;
    ListNode next = null;

    ListNode(int val) {
        this.val = val;
    }
}

```

## 合并算法

```java

public class ListNode {
    int val;
    ListNode next = null;

    ListNode(int val) {
        this.val = val;
    }
}//链表原结构定义

public class Solution {
    public ListNode Merge(ListNode list1,ListNode list2) {
        if(list1==null||list2==null)
            return list1==null?list2:list1;//判断到达链表结尾，方法把较大的节点连接在较小的节点后，然后直接返回较小的链表节点

        if(list1.val>list2.val){//将两个链表的两个节点比较
            list2.next=Merge(list1, list2.next);//将较大的节点与较小的节点后方的节点放入递归比较
            return list2;//函数返回较小的节点
        }
        else{
            list1.next=Merge(list1.next, list2);//同上
            return list1;//同上
        }
    }
}

```