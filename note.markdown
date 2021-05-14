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

*05/02/2021*

- two pointer (different direction) : must be in a sorted list or array
- kSum: check duplicate

*05/03/2021*
- two pointer (same direction) ; in place change
```
//1. pointer 'k' to reserve a position for next valid item (where to start k?)
//2. pointer 'i' to scan each item in an input array (where to start i?)
//3. if nums[i] meet the requirement of that reserved position, let nums[k] = nums[i] (what is the requirement?)
```
- array initialize
```
return new int[]{1, 2};
```

*05/12/2021*
- leetcode 27
```
 public int removeElement(int[] nums, int val) {
        int k = 0;   //reserve place for correct answer
        for (int i = 0; i < nums.length; i++) {
            if (nums[i] != val) {  //it is the correct answer
                if (k != i) { //need to swap
                    nums[k] = nums[i];
                }
                k++; // whether it need the swap or not, we need increment the reserve index
            }
            
        }
        return k;
    }
```
- when doing check duplicate, skip the first one and then loop others by 
```
num[i] != num[i - 1];
```

- two pointer 时找特定元素的距离上问题 ： 少的元素用不同index；多的话用hashmap存，之后再扫
（243， 763）

*05/13/2021*
- string -> charArray->string
```
String s = "test";
char[] c = s.toCharArray();
String s1 = new String(c);
```
- leetcode 819 string 正则表达式 整理字符串
```
s.replaceAll("\\pP", " "); //清除标点,用" "代替
s.toLowerCase(); //变小写
s.split("\\s+");//基于空格分割成String Array
```

- DO need to initialize StringBuilder array one by one after the array Initialization
