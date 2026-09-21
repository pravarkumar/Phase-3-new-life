inplace sorting algorithm -> the array is sorted with O(1) additional space

stable sorting algorithm -> the array is sorted with the equal elements values being in the same order as in the original array 


    SORTING ALGORITHMS:

<img width="382" height="55" alt="Screenshot 2026-09-21 at 8 02 34 PM" src="https://github.com/user-attachments/assets/d7f2a575-2d79-450f-bb0a-9d19b0c1a15a" />


We want to be like from the start assume we have done some prefix for the rest of the array we will iterate and see see which is the least element among them 
we will then take that element and put it in the new position thus extending the prefix.
Another invariant is to get the max in suffix and then search the res tof the intial part fot he array for the max then bring it and extend the suffix.


<img width="341" height="203" alt="image" src="https://github.com/user-attachments/assets/e335df1e-2caa-428e-ba82-3016e122c69c" />


        INPLACE 
        NOT STABLE 



<img width="269" height="66" alt="Screenshot 2026-09-21 at 8 14 53 PM" src="https://github.com/user-attachments/assets/d675bbe0-b344-4e36-aaca-2eb6af25ab6c" />


We basically in O(n) and inplace make a heap and then we constantly take the topmost element ( min heap ) and then replace the value of the topmost element by the 
bottom most element reduce the size of the array and then we bubble down again .


        INPLACE 
        NOT STABLE


Make heap in O(n):

<img width="314" height="91" alt="Screenshot 2026-09-21 at 8 19 10 PM" src="https://github.com/user-attachments/assets/48327234-9e63-46a0-a175-cf20f1c0a026" />


Basically we have the leaves already are in place if we consider only them if we consider the last two levels then we need to bubble down form the top and the 
result will be sorted and we can keep going like this till the top hence giving a simple iterative version of the make heap, making the original vector 
into a heap which we can use now to get the sorted vector.


Making of the max heap:

<img width="309" height="80" alt="Screenshot 2026-09-21 at 8 33 40 PM" src="https://github.com/user-attachments/assets/b2f8822e-42ff-4f36-a644-6b0601e6c106" />


BubbleDown:


<img width="465" height="480" alt="Screenshot 2026-09-21 at 8 33 57 PM" src="https://github.com/user-attachments/assets/d06bd4bf-b1fa-45bf-98e0-0e74b81a8e73" />


Final Sorting:


<img width="349" height="98" alt="Screenshot 2026-09-21 at 8 34 07 PM" src="https://github.com/user-attachments/assets/1f6bd807-ab9f-46de-9e7f-85b161b0c1dd" />




<img width="377" height="73" alt="Screenshot 2026-09-21 at 8 34 46 PM" src="https://github.com/user-attachments/assets/636fff02-b60c-4e11-b2c2-de9b802c035a" />


        INPLACE 
        STABLE 

<img width="413" height="293" alt="Screenshot 2026-09-21 at 8 35 28 PM" src="https://github.com/user-attachments/assets/57f53bd6-e75a-4944-b52d-c407dba41d03" />


This sorting algorithm is intutive only and the name is pretty self explanatory 



<img width="298" height="65" alt="Screenshot 2026-09-21 at 8 36 44 PM" src="https://github.com/user-attachments/assets/a651f558-39cb-41ac-9994-5d0f13a5c2dc" />


      NOT IN PLACE 
      STABLE 
      
<img width="1177" height="267" alt="Screenshot 2026-09-21 at 8 37 01 PM" src="https://github.com/user-attachments/assets/8b5d68b9-f1f9-4201-bcd0-36b7b6a22ee1" />



      DIVIDE AND CONQUER ALGOS ARE ALSO USED FOR SORTING LIKE MERGE SORT AND QUICKSORT THE GENERAL TEMPLATE IS AS FOLLOWS:


<img width="521" height="522" alt="Screenshot 2026-09-21 at 8 38 07 PM" src="https://github.com/user-attachments/assets/c241b26d-a0dc-4fcb-b8d8-09645204fa6d" />


<img width="372" height="58" alt="Screenshot 2026-09-21 at 8 38 47 PM" src="https://github.com/user-attachments/assets/882f053f-7ee8-4edc-92e0-12d614956e77" />


<img width="556" height="619" alt="Screenshot 2026-09-21 at 8 39 11 PM" src="https://github.com/user-attachments/assets/9f7930e0-7b09-47ac-853d-e382611732c2" />

But int he code we have written we are consantly allocting O(n) stpace for the temp vector its better to send it in as an argument 






