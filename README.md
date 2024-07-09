1. DuplicateZeros
Task: Given a list of integers, duplicate each zero in the list and return the result as an iterable object.
Solution: Implemented a function duplicate_zeros that iterates through the list, appending each element to a new list, and duplicating zeros when encountered. The final result is returned as an iterator.

from collections.abc import Iterable

def duplicate_zeros(donuts: list[int]) -> Iterable[int]:
    result = []
    for num in donuts:
        result.append(num)
        if num == 0:
            result.append(0)
    return iter(result)
    
2. EasyUnpack
Task: Given a tuple, return a new tuple with the first, third, and second-to-last elements.
Solution: Implemented a function easy_unpack that extracts the required elements using tuple indexing.

def easy_unpack(elements: tuple) -> tuple:
    return (elements[0], elements[2], elements[-2])
3. EvenTheLast
Task: Find the sum of elements with even indices in a list and multiply it by the last element of the list.
Solution: Implemented a function even_the_last that sums elements at even indices and multiplies the sum by the last element of the list.


def even_the_last(array: list[int]) -> int:
    if not array:
        return 0
    even_index_sum = sum(array[i] for i in range(0, len(array), 2))
    return even_index_sum * array[-1]
    
4. IndexPower
Task: Find the N-th power of the element at index N in a list. Return -1 if N is out of bounds.
Solution: Implemented a function index_power that checks if N is within bounds and returns the N-th power of the element at index N or -1 if out of bounds.

def index_power(arr: list[int], n: int) -> int:
    if n >= len(arr):
        return -1
    return arr[n] ** n
    
5. Majority
Task: Determine if the majority of elements in a list are true.
Solution: Implemented a function is_majority that counts the number of true elements and checks if it exceeds half the length of the list.

def is_majority(items: list[bool]) -> bool:
    return items.count(True) > len(items) / 2
    
Summary
All tasks were successfully implemented and tested. The solutions provided are efficient and meet the requirements of each problem statement. The use of appropriate data structures and algorithms ensures that the code is clean, readable, and maintainable.
