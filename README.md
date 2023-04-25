# Linear Search

Linear search is a simple search algorithm that checks each element in a collection, one by one, until a match is found or the entire collection has been searched.

![linear-search](https://user-images.githubusercontent.com/88421625/234402779-a15266b2-36f0-47a2-897c-47dd9a5e7fa1.gif)


## Key Points
Here are some important points about linear search:

•	Linear search is a simple search algorithm that checks each element in a collection one by one until a match is found or the entire collection has been searched.

•	Linear search has a time complexity of O(n), where n is the size of the collection being searched. This means that the time taken by the algorithm to search the collection grows linearly with the size of the collection.

•	Linear search is best suited for small collections or unsorted collections. For larger or sorted collections, other search algorithms like binary search are more efficient.

•	Linear search can be implemented using a loop to iterate over each element in the collection, or using recursion to recursively search through the collection.

•	If the collection being searched is sorted, a binary search algorithm can be used instead, which has a time complexity of O(log n) and is much more efficient for large collections.

•	Linear search can be used on any collection of data types, including arrays, linked lists, and trees.

•	In some cases, linear search can be optimized by performing a "sentinel search" which involves placing the search key at the end of the collection, thereby avoiding the need for an explicit boundary check in the loop.

•	Linear search can be useful as a simple and quick way to search a small collection or to check if an item is present in an unsorted collection.

Here's an example of a linear search implementation in C:

```bash
#include <stdio.h>

int linear_search(int arr[], int n, int x) {
    for(int i = 0; i < n; i++) {
        if(arr[i] == x) {
            return i; // return the index of the found element
        }
    }
    return -1; // element not found
}

int main() {
    int arr[] = {1, 5, 7, 12, 15};
    int n = sizeof(arr)/sizeof(arr[0]);
    int x = 12;
    int result = linear_search(arr, n, x);
    if(result == -1) {
        printf("Element not found");
    }
    else {
        printf("Element found at index %d", result);
    }
    return 0;
}
```
In this example, the 'linear_search' function takes an array 'arr', the size of the array 'n', and the element to search for 'x' as arguments. It then iterates over each element in the array, comparing it to the search element 'x'. If a match is found, it returns the index of the found element. If the entire array has been searched and the element is not found, it returns '-1'.

In the 'main' function, an array 'arr' is declared and initialized with values, along with the size of the array 'n' and the element to search for 'x'. The 'linear_search' function is called with these arguments, and the result is stored in the result variable. Finally, the result is printed to the console.






## Code:
```bash
// implementing linear search

#include <stdio.h>
#include <stdlib.h>

int main()
{
	int arr[10] = {3, 7, 100, 45, 40, 45, 476, 40, 9, 31};
	//int arr[10] = {rand(), rand(), rand(), rand(), rand(), rand(), rand(), rand(), rand(), rand()};

	int n;
	int count = 0;
	
	// array to store the indices at which the entered element is found (if it is found)
	int index[10] = {-1, -1, -1, -1, -1, -1, -1, -1, -1, -1};
	
	int i;
	
	printf("Enter a number: ");
	scanf("%d", &n);
	printf("\n");
	
	for(i = 0; i < 10; i++)
	{
		if(arr[i] == n)
		{
			index[i] = i;
			count++;
		}
	}
	
	if(count >= 1)
	{
		printf("Element found at index / indices: ");
		
		for(i = 0; i < 10; i++)
		{
			if(index[i] != -1)
			{
				printf("%d ", index[i]);
			}
		}
		printf("\n");
	}
	else
	{
		printf("Element not found.\n");
	}
	
	
	
	/*
	if(count >= 1)
	{
		printf("Element found at index: %d\n", index);
		//printf("Element found at %d indices.\n\n", count);
	}
	else
	{
		printf("Element not found.");
	}
	*/
	
	/*
	// finding the indices at which the element is found
	int *indices = (int*)calloc(count, sizeof(int));
	
	for(i = 0; i < 10; i++)
	{
		if(arr[i] == n)
		{
			indices[i] = i;
		}
	}
	
	printf("Indices at which the entered element was found: ");
	
	for(i = 0; i < 10; i++)
	{
		if(indices[i] >= 0 && indices[i] <= 9)
		{
			printf("%d ", indices[i]);			
		}
	}
	*/
	
	return 0;
	
}
```
## Output
![Screenshot 2023-04-26 021653](https://user-images.githubusercontent.com/88421625/234402269-ba87fe63-3337-4d6f-aa89-91d080a92a25.png)

![Screenshot 2023-04-26 021723](https://user-images.githubusercontent.com/88421625/234402282-558fd7bc-3214-4403-bb76-20df537db155.png)

![Screenshot 2023-04-26 021743](https://user-images.githubusercontent.com/88421625/234402288-64eb1314-425d-4c26-be14-c7573f170387.png)
