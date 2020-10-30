# QUICKSORT
In QuickSort we first partition the array in place such that all elements to the left of the pivot element are smaller, while all elements to the right of the pivot are greater that the pivot. Then we recursively call the same procedure for left and right subarrays.

```java

public static void quicksort(int[] arr, int lo, int hi) {

        if (lo >= hi) {
            return;
        }
        // partitioning
        int mid = (lo + hi) / 2;
        int pivot = arr[mid];

        int left = lo;
        int right = hi;

        while (left <= right) {

            while (arr[left] < pivot)
                left++;
            while (arr[right] > pivot)
                right--;

            if (left <= right) {
                int temp = arr[left];
                arr[left] = arr[right];
                arr[right] = temp;
                left++;
                right--;
            }
        }

        quicksort(arr, lo, right);
        quicksort(arr, left, hi);
    }
```
