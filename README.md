def calculate_gap(numbers):
    max_gap = 0
    gap = 0
    
    # Sort the list of numbers
    numbers.sort()
    
    # Calculate the gap
    for i in range(len(numbers) - 1):
        current_gap = numbers[i + 1] - numbers[i]
        
        if current_gap > 1:
            gap = current_gap - 1
            if gap > max_gap:
                max_gap = gap
    
    return max_gap

# قم بإدخال قائمة الأرقام هنا
numbers_list = [5, 10, 15, 20, 30]

# اطبع الفجوة القصوى
print("الفجوة القصوى في القائمة هي:", calculate_gap(numbers_list))
