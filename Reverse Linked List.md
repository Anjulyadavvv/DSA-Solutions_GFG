## 01. Reverse Linked List

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/reverse-a-linked-list/1)

### Problem Description

**Task:** Given the head of a singly linked list. Reverse the linked list and return the head of the reversed list.Examples:Input:

#### Examples

##### Example 1

- **Output:**
```text
8 - > 9 - > 10 - > 7 - > 2Explanation: After reversing the linked listInput: Output: 8
```

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (C++)

- **Submitted:** 2026-11-14 09:35:49
- **Status:** Correct
- **Marks:** 2

```cpp
/* Structure of Linked List Node
class Node {
 public:
    int data ;
    Node *next ;

    Node(int x) {
        data = x ;
        next = nullptr ;
    }
};
*/

class Solution {
  public:
    Node* reverseList(Node* head) {
        // code here
        Node*curr=head,*prev=NULL,*fut=NULL;
        
        while(curr)
        {
            fut=curr->next;
           curr->next=prev;
           prev=curr;
           curr=fut;
            
        }
        head=prev;
        return head;
        
    }
};
```

*Generated on: 18/11/2026, 23:44:49*