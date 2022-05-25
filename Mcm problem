#include <stdio.h>
void printArray(int a[], int n)
{
    int i;
    for (i = 0; i < n; i++)
    {
        printf("%d ",a[i]);
    }
    printf("\n");
}
void quick_sort(int a[], int left, int right)
{
    int i = left, j = right;
    int pivot = i;                  
    while (i < j)
    {
        if (pivot == i)
        {
            if (a[pivot] > a[j])
            {
                int tmp = a[pivot];
                a[pivot] = a[j];
                a[j] = tmp;
                pivot = j;
            }
            else
            {
                j--;
            }
        }
        else
        {
            if (a[pivot] < a[i])
            {
                int tmp = a[pivot];
                a[pivot] = a[i];
                a[i] = tmp;
                pivot = i;
            }
            else
            {
                i++;
            }
        }
    }
    if (pivot + 1 <= right && pivot - 1 >= left)
    {
        quick_sort(a, left, pivot - 1);
        quick_sort(a, pivot + 1, right);
    }
    else if (pivot + 1 <= right)
    {
        quick_sort(a, pivot + 1, right);
    }
    else if (pivot - 1 >= left)
    {
        quick_sort(a, left, pivot - 1);
    }
}
int main()
{
    int arr[] = {12, 3, 5, 13, 18, 0, 6, 15, 14, 4};
    int lb = 0;
    int n = sizeof(arr) / sizeof(arr[0]);
    printArray(arr, n);
    quick_sort(arr, lb, n - 1);
    printArray(arr, n);
}
