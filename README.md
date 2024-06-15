
def getval(arr):
  if len(arr) <=1:
    return arr
  
  
  else:
    pivot = arr[0]
    less = [x for x in arr[1:] if x<=pivot]
    greater= [x for x in arr[1:] if x>pivot]
    return getval(less) + [pivot]+getval(greater)



arr=[8,4,2,1]
ans = getval(arr)
print(ans)
