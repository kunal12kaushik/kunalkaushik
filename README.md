# kunalkaushik
/*Program From ApkZube*/

58. Merge sort algorithm

def mergeSort(nlist):
    print("Splitting ",nlist)
    if len(nlist)>1:
        mid = len(nlist)//2
        lefthalf = nlist[:mid]
        righthalf = nlist[mid:]

        mergeSort(lefthalf)
        mergeSort(righthalf)
        i=j=k=0       
        while i < len(lefthalf) and j < len(righthalf):
            if lefthalf[i] < righthalf[j]:
                nlist[k]=lefthalf[i]
                i=i+1
            else:
                nlist[k]=righthalf[j]
                j=j+1
            k=k+1

        while i < len(lefthalf):
            nlist[k]=lefthalf[i]
            i=i+1
            k=k+1

        while j < len(righthalf):
            nlist[k]=righthalf[j]
            j=j+1
            k=k+1
    print("Merging ",nlist)

nlist = [14,46,43,27,57,41,45,21,70]
mergeSort(nlist)
print(nlist)



>>Output:

Splitting  [14, 46, 43, 27, 57, 41, 45, 21, 70]                                                               
Splitting  [14, 46, 43, 27]                                                                                   
Splitting  [14, 46]                                                                                           
Splitting  [14]                                                                                               
Merging  [14]                                                                                                 
Splitting  [46]                         
-------
Merging  [14, 21, 27, 41, 43, 45, 46, 57, 70]                                                                 
[14, 21, 27, 41, 43, 45, 46, 57, 70] 
#Merge sort #algorithm
