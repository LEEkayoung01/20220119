# 20220119

# 점프투파이썬 05-1. 클래스
1) 클래스를 어떻게 만들지 먼저 구상하기
>>> a = FourCal()
>>> a.setdata(4, 2)
>>> print(a.add())   # 6
>>> print(a.mul())   # 8
>>> print(a.sub())   # 2
>>> print(a.div())   # 2

2) 클래스 구조 만들기 
>>> class FourCal:
>>>   def setdata(self, first, second):
>>>       self.first = first
>>>       self.second = seconds
a-> self, 4-> first, 2-> second

>>>   def add(self):
>>>       result = self.first + self.second
>>>       return result

3) 생성자 (Constructor)
>>> def __init__(self, first, second):
>>>     self.first = first
>>>     self.second = second

4) 클래스 상속
>>> class MoreFourCal(FourCal):
>>>   def pow(self):
>>>       result = self.first ** self.second
>>>       return result

5) 클래스 변수
- 클래스이름.클래스변수
>>> class Family:
>>>     lastname = "김"

>>> print(Family.lastname)   # 김

# LeetCode (2) Add two numbers
1) 
///
# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, val=0, next=None):
#         self.val = val
#         self.next = next
class Solution:
    def addTwoNumbers(self, l1: Optional[ListNode], l2: Optional[ListNode]) -> Optional[ListNode]:
        while l1.next:
            num1 += l1.val * (10**val)
            val++
        val = 0
        while l2.next:
            num2 += l2.val * (10**val)
            val++
        num_result = num1+num2
        ListNode(num_result)
        return num_result
        
2) 예시코드
# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, val=0, next=None):
#         self.val = val
#         self.next = next
class Solution:
    def addTwoNumbers(self, l1: Optional[ListNode], l2: Optional[ListNode]) -> Optional[ListNode]:
        # 초기화
        result = ListNode(0)
        result_tail = result
        carry = 0
        
        while l1 or l2 or carry:
            val1 = (l1.val if l1 else 0)   # 자릿수가 다를 때를 대비
            val2 = (l2.val if l2 else 0)
            carry, out = divmod(val1 + val2 + carry, 10)
            
            result_tail.next = ListNode(out)
            result_tail = result_tail.next
            
            l1 = (l1.next if l1 else None)
            l2 = (l2.next if l2 else None)
            
        return result.next
        
- 마지막에 result_tail을 이용하는 것이 아니라 result.next 반환하는 이유가 이해가 안 된다. 

3) 예시코드2 - 유튜브 NeetCode
# Definition for singly-linked list.
# class ListNode:
#   def __init__(self, val=0, next=None):
#     self.val = val
#     self.next = next
class Solution:
    def addTwoNumbers(self, l1:ListNode, l2: ListNode)-> ListNode
        dummy = ListNode()
        cur = dummy
     
    carry = 0
    while l1 or l2 or carry:
        v1 = l1.val if l1 else 0
        v2 = l2.val if l2 else 0
        
        # new digit
        val = v1 + v2 + carry
        carry = val // 10
        val = val % 10
        cur.next = ListNode(val)
        
        # update ptrs
        cur = cur.next
        l1 = l1.next if l1 else None
        l2 = l2.next if l2 else None
        
    return dummy.next

