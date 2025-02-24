# Data Structures and Algorithms
## Arrays and Strings

### Creating Arrays and Strings in C++: Methods, Tips & Tricks

**Creating Arrays in C++**

**Best Practice:** Always initialize arrays to avoid undefined behavior.

## Looping Through Arrays
```cpp
int arr[] = {10, 20, 30, 40, 50};

// Traditional for loop
for (int i = 0; i < 5; i++) {
    std::cout << arr[i] << " ";
}

// Range-based for loop (C++11+)
for (int num : arr) {
    std::cout << num << " ";
}
```

**Tip:** Prefer range-based loops for readability when you don’t need an index.

## Multi-Dimensional Arrays
```cpp
int matrix[2][3] = {
    {1, 2, 3},
    {4, 5, 6}
};

// Accessing elements
std::cout << matrix[1][2]; // Prints 6
```

**Best Practice:** Use constants for dimensions to improve maintainability.

## Passing Arrays to Functions
```cpp
void printArray(const int arr[], int size) {
    for (int i = 0; i < size; i++) {
        std::cout << arr[i] << " ";
    }
}
```

**Tip:** Always pass the array size separately; C++ doesn’t track array sizes.

## Dynamic Arrays (Heap Allocation)
```cpp
int* dynamicArray = new int[5]; // Allocate array dynamically

delete[] dynamicArray; // Free memory
```

**Best Practice:** Always `delete[]` dynamically allocated arrays to prevent memory leaks.

## Using `std::array` (C++11+)
```cpp
#include <array>

std::array<int, 5> arr = {1, 2, 3, 4, 5};
std::cout << arr[2]; // Access elements safely
```

**Why use `std::array`?**  
- Provides safer indexing (`.at()`)
- Supports `.size()`, unlike raw arrays

## Using `std::vector` (Dynamic Size)
```cpp
#include <vector>

std::vector<int> vec = {1, 2, 3, 4};
vec.push_back(5);  // Append element
std::cout << vec.size(); // Get size dynamically
```

**Why use `std::vector`?**  
- **Resizes automatically**  
- **Built-in methods like `.size()`, `.push_back()`, and `.erase()`**  
- **Prevents memory leaks when used correctly**  

---

## Summary of Best Practices
**Prefer `std::array` over raw arrays for fixed sizes**  
**Use `std::vector` for dynamic arrays**  
**Initialize arrays to avoid garbage values**  
**Use range-based loops for cleaner code**  
**Always free dynamically allocated memory (`delete[]`)**  

---
```

