def selection_sort(arr):
    """
    Sorts a list in ascending order using the Selection Sort algorithm.
    Modifies the list in-place.
    """
    n = len(arr)
    
    # Traverse through all array elements
    for i in range(n - 1):
        # Find the minimum element in the remaining unsorted array
        min_index = i
        for j in range(i + 1, n):
            if arr[j] < arr[min_index]:
                min_index = j
                
        # Swap the found minimum element with the first element of the unsorted part
        if min_index != i:
            arr[i], arr[min_index] = arr[min_index], arr[i]
            
    return arr

# Example usage to verify the code works without errors
if __name__ == "__main__":
    test_list = [64, 25, 12, 22, 11]
    print("Original list:", test_list)
    
    sorted_list = selection_sort(test_list)
    print("Sorted list:  ", sorted_list)
    
