# week-11_final_draft
//Write a function that takes an array of integers and returns the maximum element in the array.

def find_max(arr):
    max_element = arr[0]
    for element in arr:
        if element > max_element:
            max_element = element
    return max_element

numbers = [3, 5, 7, 2, 8, -1, 4, 10, 12]
print("Maximum element:", find_max(numbers))

//Write a function that reverses the elements of an array.
def reverse_array(arr):
    start = 0
    end = len(arr) - 1
    while start < end:
        arr[start], arr[end] = arr[end], arr[start]
        start += 1
        end -= 1
    return arr

numbers = [1, 2, 3, 4, 5]
print("Reversed array:", reverse_array(numbers))
//Write a function that calculates the sum of all elements in an array.

def sum_array(arr):
    total = 0
    for element in arr:
        total += element
    return total

numbers = [1, 2, 3, 4, 5]
print("Sum of array elements:", sum_array(numbers))

//Write a function that finds the second largest element in an array.
def find_second_largest(arr):
    if len(arr) < 2:
        return None

    first = second = float('-inf')
    for element in arr:
        if element > first:
            second = first
            first = element
        elif element > second and element != first:
            second = element
    return second
numbers = [12, 35, 1, 10, 34, 1]
print("Second largest element:", find_second_largest(numbers))

//Write a function that merges two sorted arrays into a single sorted array.
def merge_sorted_arrays(arr1, arr2):
    merged_array = []
    i = j = 0

    while i < len(arr1) and j < len(arr2):
        if arr1[i] < arr2[j]:
            merged_array.append(arr1[i])
            i += 1
        else:
            merged_array.append(arr2[j])
            j += 1

    while i < len(arr1):
        merged_array.append(arr1[i])
        i += 1

    while j < len(arr2):
        merged_array.append(arr2[j])
        j += 1

    return merged_array

arr1 = [1, 3, 5, 7]
arr2 = [2, 4, 6, 8]
print("Merged sorted array:", merge_sorted_arrays(arr1, arr2))


