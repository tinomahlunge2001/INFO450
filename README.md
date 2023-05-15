# INFO450
#part 1 


with open('numbers.txt', 'r') as file:
    L = file.readlines()
print(L)

#part 2 

def sum_recursive(n):
    if n == 1:
        return 1
    else:
        return n + sum_recursive(n - 1)
n = 5
result = sum_recursive(n)
print(f"The sum of all integers from 1 to {n} is: {result}")

#part 3 

def looping(lst):
    summed_lst = []
    for num in lst:
        summed_num = sum_recursive(num)
        summed_lst.append(summed_num)
    return summed_lst
numbers = [2, 5, 3]
result = looping(numbers)
print(f"The recursively summed list is: {result}")


#part 4 

def sum_recursive(n):
    if n == 1:
        return 1
    else:
        return n + sum_recursive(n - 1)

def looping(lst):
    summed_lst = []
    for num in lst:
        summed_num = sum_recursive(num)
        summed_lst.append(summed_num)
    return summed_lst


with open('numbers.txt', 'r') as file:
    L = [int(line.strip()) for line in file.readlines()]


result = looping(L)


print(result)
