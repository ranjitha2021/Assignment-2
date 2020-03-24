

'''
   Finding the repeated values after reading the number from a file.


'''

def printRepeating (arr, size): 
  
    print("Repeating elements are \n",end = '') 
    for i in range (0, size): 
        for j in range (i + 1, size): 
            if arr[i] == arr[j]: 
                print(arr[i],"\n", end = '') 
      
# Driver code 
arrList=[]

try:
    f=open('numlist.txt',"r")  


    for line in f:
        arrList.append (int (line.strip('\n')))

    f.close()
    
    arr_size = len (arrList)
    printRepeating (arrList, arr_size)
except:
    print("File not found")
    
