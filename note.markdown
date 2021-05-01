## Note

*04/30/2021/*

- Arraylist to List
```
ArrayList<Object> list = Arrays.asList("array");
```

- from small to big (number)
```
list.sort((a, b) -> a - b);
//[0,1,2,3,4]
```

- Arrays.copyOfRange(int []original,int start,int end)
return an array from start of original to end of original, start is included but end is NOT included.

- PriorityQueue, small -> big, keep track the smallest
```
PriorityQueue<Integer> pq = new PriorityQueue<>((a, b) -> a - b);
```

- set dummy node when the LinkList problem occurs
```
ListNode dummy = new ListNode(-1);
dummy.next = head
ListNode cur = dummy;
```

- reverse linkedList
three Node : cur, pre, next
```
//cur = head, current node
//pre = null, as the pre node of each new add node of the return list
//next = cur.next, record the next node of the cur node
//cur pointed to next -> point to pre
```