# Sıralama Algoritmaları
Insertion Sort, Merge Sort and  Binary Search Tree

## Insertion Select 

![ ](https://upload.wikimedia.org/wikipedia/commons/0/0f/Insertion-sort-example-300px.gif)

    void InsertionSort<T>(T[] array) where T :  IComparable
        {
            for(int i = 1; i < array.Length; i++)
            {
                T key = array[i];
                int j = i - 1;
                while(j >= 0 && array[j].CompareTo(key) > 0)
                {
                    array[j + 1] = array[j];
                    j--;
                }
                array[j + 1] = key;
            }
        }

Soru - 1  `[22,27,16,2,18,6]`

    Step 1: [22,27,16,2,18,6]   
    Step 2: [22,16,27,2,18,6]   
    Step 3: [16,22,27,2,18,6]   
    Step 4: [16,22,2,27,18,6]   
    Step 5: [16,2,22,27,18,6]   
    Step 6: [2,16,22,27,18,6]   
    Step 7: [2,16,22,18,27,6]   
    Step 8: [2,16,18,22,27,6]   
    Step 9: [2,16,18,22,6,27]   
    Step 10: [2,16,18,6,22,27]  
    Step 11: [2,16,6,18,22,27]  
    Step 12: [2,6,16,18,22,27]  

#### Big-O gösterimi
                                     O(n^2)
####  Time Comlexity: Dizi sıralandıktan sonra 18 sayısı case'lerden hangisinin kapsamına girer ?   
      Average Case         

## Merge Sort

![](https://upload.wikimedia.org/wikipedia/commons/c/cc/Merge-sort-example-300px.gif)

Soru - 2 `[16,21,11,8,12,22]`

Answer : 

    Step 1:  [16, 21, 11, 8, 12, 22]

    Step 2:  [16, 21, 11] - [8, 12, 22]

    Step 3:  [16, 21] - [11] - [8, 12] - [22] 

    Step 4:  [16] - [21] - [11] - [8] - [12] - [22]

    Step 5:  [16, 21] - [8, 11] - [12, 22]

    Step 6:  [8, 11, 16, 21] - [12, 22]

                  [8, 11, 12, 16, 21, 22]                                
                          
                        
             
                                               
                               

### Big-O gösterimi
                                     O(nlogn)

## Binary Search Tree

![](https://upload.wikimedia.org/wikipedia/commons/9/9b/Binary_search_tree_example.gif)

Soru - 3 `[7, 5, 1, 8, 3, 6, 0, 9, 4, 2]` 

                7 
              /   \ 
            5      8 
          /   \      \ 
         1     6     9 
       /   \ 
     0      3 
          /   \ 
         2      4 
