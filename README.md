# array-insertion
#include <iostream>
using namespace std;

int main() {
    int arr[100] = {10, 20, 30, 40, 50}; 
    int size = 5; 
    int element, position;
    cout << "Original array: ";
    for (int i = 0; i < size; i++) {
        cout << arr[i] << " ";
    }
    cout << endl;
    cout << "Enter the element to insert: ";
    cin >> element;
    cout << "Enter the position (1 to " << size + 1 << ") where you want to insert: ";
    cin >> position;

    if (position < 1 || position > size + 1) {
        cout << "Invalid position! Insertion not possible." << endl;
    } else {
        int index = position - 1;
        for (int i = size - 1; i >= index; i--) {
            arr[i + 1] = arr[i];
       }
        arr[index] = element;
        size++;
        cout << "Array after insertion: ";
        for (int i = 0; i < size; i++) {
            cout << arr[i] << " ";
        }
        cout << endl;
    }

    return 0;
}
  
