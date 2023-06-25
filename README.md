question 1-Move zeroes 
def moveZeroes(nums):
    """
    Move zeroes to the end of the array while maintaining the relative order of the non-zero elements.
    
    Args:
        nums (List[int]): The input integer array.
    
    Returns:
        None (Modifies the input array in-place)
    """
    # Initialize a pointer to keep track of the last non-zero element index
    last_non_zero_index = 0
    
    # Iterate through the array
    for i in range(len(nums)):
        # If the current element is non-zero, swap it with the element at the last non-zero index
        if nums[i] != 0:
            nums[last_non_zero_index], nums[i] = nums[i], nums[last_non_zero_index]
            last_non_zero_index += 1
            nums = [0, 1, 0, 3, 12]
moveZeroes(nums)
print(nums)  # Output: [1, 3, 12, 0, 0]
question 2- 
def firstUniqChar(s):
    
    char_freq = {}

   
    for char in s:
        char_freq[char] = char_freq.get(char, 0) + 1

    
    for i in range(len(s)):
        if char_freq[s[i]] == 1:
            return i

    
    return -1
