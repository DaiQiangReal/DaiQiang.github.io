---
layout: post
title: 采用栈结构，递归实现链表的反转
categories: [算法]
description: 采用栈结构，递归实现链表的反转
keywords: 栈，递归，链表，反转链表
---
#采用栈结构，递归实现链表的反转
##需要反转链表原结构

```java

public class ListNode {
    int val;
    ListNode next = null;

    ListNode(int val) {
        this.val = val;
    }
}
```

###代码

```java

import java.util.Stack;
public class ListNode {
    int val;
    ListNode next = null;
    ListNode(int val) {
        this.val = val;
    }
}//链表原结构

public class Solution {
    public ListNode do_reverse(Stack<ListNode> data)
    {
        ListNode ans=data.pop();
        if(data.empty())
        {
            ans.next=null;
            return ans;
        }
        ans.next=do_reverse(data);
        return ans;
    }//递归反转链表核心代码

    public ListNode ReverseList(ListNode head) 
    {
        if(head==null)
            return null;
        Stack<ListNode> data=new Stack<ListNode>();//下方循环将原链表所有节点压栈，方便反转
        while(true)//循环压栈
        {
            if(head.next==null)
            {
                data.push(head);
                break;
            }
            data.push(head);
            head=head.next;
        }
        return do_reverse(data);//调用核心反转函数
        
    }//采用栈结构，调用核心反转函数代码
}
```