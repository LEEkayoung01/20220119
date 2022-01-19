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


