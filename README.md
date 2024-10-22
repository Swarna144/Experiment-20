# Experiment-20
Aim:
To study and implement Sorting Algorithm.

Theory:
Sorting is a way to arrange elements in a particular order. We will be understand 3 types of sorting which are:
→ Selection Sort
→ Insertion Sort
→ Bubble Sort


Selection Sort: A simple comparison-based sorting algorithm. It sorts an array by repeatedly finding the minimum element from the unsorted portion of the array and placing it at the beginning.
Selection Sort Steps:

1)Find the smallest element in the unsorted array.

2)Swap it with the first element of the unsorted array.

3)Move the boundary between the sorted and unsorted parts by one element.

4)Repeat the process until the array is sorted.

Insertion Sort: This works by repeatedly taking an element from the unsorted portion and inserting it into its correct position within the sorted portion of the array.
Insertion Sort Steps:

1)Assume the first element is sorted.

2)Take the next element and compare it with the elements in the sorted portion.

3)Shift all larger elements in the sorted part to the right.

4)Insert the current element in its correct position.

5)Repeat the process for all elements.

CODE:-

20
```
#include<iostream>
using namespace std;

int factorial(int n);

int main() {

  int n;

  cout << "Enter a positive integer: ";
  cin >> n;

  cout << "Factorial of " << n << " = " << factorial(n);

  return 0;
}

int factorial(int n) {
  if(n > 1)
    return n * factorial(n - 1);
  else
    return 1;
}
```

20A
```
#include <iostream>
using namespace std;

void insertionSort(int arr[], int n) {
    for (int i = 1; i < n; i++) {
        int key = arr[i];
        int j = i - 1;

        while (j >= 0 && arr[j] > key) {
            arr[j + 1] = arr[j];
            j--;
        }
        arr[j + 1] = key;
    }
}

int main() {
    int arr[] = {64, 25, 12, 22, 11};
    int n = sizeof(arr) / sizeof(arr[0]);

    cout << "Original array: ";
    for (int i = 0; i < n; i++) {
        cout << arr[i] << " ";
    }

    insertionSort(arr, n);

    cout << "\nSorted array: ";
    for (int i = 0; i < n; i++) {
        cout << arr[i] << " ";
    }
```

20B
```
#include<iostream>
using namespace std;

void swap(int* a,int* b){
    int temp;
    temp=*a;
    *a=*b;
    *b=temp;
}
int main(){
    int elements;
    cout<<"How many elements in the array? :";
    cin>>elements;
    int array[elements];
    cout<<"Enter elements:";
    for(int i=0;i<elements;i++){
        cin>>array[i];
    }
    for(int i=0;i<elements;i++){
        cout<<array[i]<<" ";
    }
    int n=0;
    while(n!=elements){
        for(int i=0;i<elements-n;i++){
            if(array[i]>array[i+1]){
                swap(&array[i],&array[i+1]);
            }
        }
        n++;
    }
    cout<<"\nSorted array is:"<<endl;
    for(int i=0;i<elements;i++){
        cout<<array[i]<<" ";
    }
    return 0;
}
```


