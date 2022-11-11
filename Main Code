

# big O notation - O(n)
def linear_search(l,target):
    for i in range (len(l)):
        if l[i]==target:
            return [i]
    return -1

#binary seach algorithm is a divide and conqure algorithm that helps to search a list
#binary search has to be in order to work
# big O notation - O(log n)
def binary_search(l,target,low=None,high=None):
    if low is None:
        low = 0
    if high is None:
        high = len(l)-1
    
    if high < low:
        return -1
    #example l = [1,3,5,7,9]
    midpoint = (low+high) //2 # ths // gives a whole number
    if l[midpoint] ==target:
        return [midpoint]
    elif target<l[midpoint]:
        return binary_search(l,target,low,midpoint-1)
    else:
        # target > l[midpoint]
        return binary_search(l,target,midpoint+1,high)


def binary_search_without_recursion(my_list, elem):
   low = 0
   high = len(my_list) - 1
   mid = 0
   while low <= high:
      mid = (high + low) // 2 # goes to middle of the list
      if my_list[mid] < elem: # if middle is less than target
         low = mid + 1 #low is middle + 1
      elif my_list[mid] > elem:# if middle is greater than target
         high = mid - 1#high is middle - 1
      else:
         return [mid] # send the answer
   return -1
#interpolian search - improved version of binary search - explained on this video https://www.youtube.com/watch?v=iMVKo1vXVsw 
# with recursion
#formula = left+(right-left)/(arr(right)-arr(left))*(key-arr(left))
#left meaning begining of the list
#right meaning the amount of items in the list, in our case it will be 5

# If x is present in arr[0..n-1], then
# returns index of it, else returns -1.


def interpolationSearch(arr, lo, hi, x):

	# Since array is sorted, an element present
	# in array must be in range defined by corner
	if (lo <= hi and x >= arr[lo] and x <= arr[hi]):
		# Probing the position with keeping
		# uniform distribution in mind.
		pos = lo + ((hi - lo) // (arr[hi] - arr[lo]) *
					(x - arr[lo]))
		# Condition of target found
		if arr[pos] == x:
			return [pos]

		# If x is larger, x is in right subarray
		if arr[pos] < x:
			return interpolationSearch(arr, pos + 1,
									hi, x)
		# If x is smaller, x is in left subarray
		if arr[pos] > x:
			return interpolationSearch(arr, lo,
									pos - 1, x)
	return -1

# Driver code
# This code is contributed by Hardik Jain https://www.geeksforgeeks.org/interpolation-search/



l = [1,3,5,7,9,11,13,17]
target = 8
print(linear_search(l,target))
print(binary_search(l, target))
print ( binary_search_without_recursion(l, target))
print(interpolationSearch(l, 0, len(l)-1 , target))

