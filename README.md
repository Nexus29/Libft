# 📚 Libft: The 42 School Custom C Library

[![C Language Badge](https://img.shields.io/badge/Language-C-blue.svg)](https://en.wikipedia.org/wiki/C_(programming_language))
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

### 🌟 Project Overview

This repository contains **Libft** , the first major project of the **42 Common Core curriculum**.

The objective of this project is to create a custom C library (`libft.a`) that re-implements a select number of functions from the standard C library (`libc`) and includes additional utility functions for string, memory, and list manipulation. This library will be used and relied upon for all subsequent C projects within the 42 curriculum.

The project is designed to deepen the understanding of:
* **Pointers and Memory Allocation** (using `malloc`, `free`, etc.).
* **The C Standard Library** functions and their inner workings.
* **Creating and managing static libraries** (`.a` files).

---

### 🛠️ Installation and Usage

To use this library in your own C projects:

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/Nexus29/42-libft.git](https://github.com/Nexus29/42-libft.git)
    cd 42-libft
    ```

2.  **Compile the Library:**
    Run `make` to compile the mandatory functions and create the static library file, `libft.a`.
    ```bash
    make
    ```
    *(Optional: Run `make bonus` to include the linked list functions)*

3.  **Use it in Your Project:**
    To compile your own C file (`main.c`) with `libft.a`, you need to include the header and link the library.

    **In your C file (`main.c`):**
    ```c
    #include "libft.h" 
    // ... use your ft_ functions
    ```

    **Compilation command:**
    ```bash
    gcc -Wall -Wextra -Werror main.c -L. -lft -I. -o my_program
    ```
    * `-L.`: Tells the compiler to look for libraries in the current directory.
    * `-lft`: Links the `libft.a` library (the `-l` flag drops the `lib` prefix and the `.a` extension).
    * `-I.`: Tells the compiler to look for the header file (`libft.h`) in the current directory.

---

### 📜 Implemented Functions

The functions are divided into three main categories. (***Note:*** *These are the typical functions; ensure you've completed all of them in your final version.*)

#### **Part 1: Functions from $\text{libc}$ (The C Standard Library)**

| Function Name | Description |
| :--- | :--- |
| `ft_isalpha` | Checks for an alphabetic character. |
| `ft_isdigit` | Checks for a digit (0 through 9). |
| `ft_isalnum` | Checks for an alphanumeric character. |
| `ft_isascii` | Checks whether c is a 7-bit US-ASCII character. |
| `ft_isprint` | Checks for any printable character. |
| `ft_strlen` | Computes the length of the string s. |
| `ft_memset` | Fills the first n bytes of the memory area pointed to by s with the constant byte c. |
| `ft_bzero` | Writes n zeroed bytes to the memory area starting at s. |
| `ft_memcpy` | Copies n bytes from memory area src to memory area dst. |
| `ft_memmove` | Copies len bytes from string src to string dst. The memory areas may overlap. |
| `ft_strlcpy` | Copies strings with a defined size limit. |
| `ft_strlcat` | Concatenates strings with a defined size limit. |
| `ft_toupper` | Converts a lowercase letter to the corresponding uppercase letter. |
| `ft_tolower` | Converts an uppercase letter to the corresponding lowercase letter. |
| `ft_strchr` | Locates the first occurrence of c in the string s. |
| `ft_strrchr` | Locates the last occurrence of c in the string s. |
| `ft_strncmp` | Compares not more than n characters of two strings. |
| `ft_memchr` | Locates the first occurrence of c in the first n bytes of string s. |
| `ft_memcmp` | Compares byte string s1 against byte string s2. |
| `ft_strnstr` | Locates the first occurrence of the null-terminated string needle in the string haystack. |
| `ft_atoi` | Converts the initial portion of the string pointed to by str to int. |
| `ft_calloc` | Allocates memory for an array and initializes it to zero. |
| `ft_strdup` | Duplicates a string. |

#### **Part 2: Additional Functions**

| Function Name | Description |
| :--- | :--- |
| `ft_substr` | Allocates and returns a substring from the string 's'. |
| `ft_strjoin` | Allocates and returns a new string, which is the result of the concatenation of 's1' and 's2'. |
| `ft_strtrim` | Allocates and returns a copy of 's1' with the characters specified in 'set' removed from the beginning and the end of the string. |
| `ft_split` | Allocates and returns an array of strings obtained by splitting 's' using the character 'c' as a delimiter. |
| `ft_itoa` | Allocates and returns a string representing the integer received as an argument. |
| `ft_strmapi` | Applies a function to each character of a string to create a new string. |
| `ft_striteri` | Applies a function to each character of a string. |
| `ft_putchar_fd` | Outputs the character 'c' to the given file descriptor. |
| `ft_putstr_fd` | Outputs the string 's' to the given file descriptor. |
| `ft_putendl_fd` | Outputs the string 's' to the given file descriptor, followed by a newline. |
| `ft_putnbr_fd` | Outputs the integer 'n' to the given file descriptor. |

#### **Bonus Part: Linked List Functions**

These functions are compiled with `make bonus` and deal with the custom `t_list` structure.

| Function Name | Description |
| :--- | :--- |
| `ft_lstnew` | Creates a new list node. |
| `ft_lstadd_front` | Adds the node 'new' at the beginning of the list. |
| `ft_lstsize` | Counts the number of elements in a list. |
| `ft_lstlast` | Returns the last element of the list. |
| `ft_lstadd_back` | Adds the node 'new' at the end of the list. |
| `ft_lstdelone` | Takes as a parameter a node and frees the memory of the node's content. |
| `ft_lstclear` | Deletes and frees all nodes in a list. |
| `ft_lstiter` | Applies a function to the content of each node. |
| `ft_lstmap` | Applies a function to the content of all nodes and returns a new list. |

---

### 👤 Author

* **Giovanni Pio Lancellotta** - [Nexus29](https://github.com/Nexus29)
    * `42 Student ID:` **glancell**
    * `Personal Website:` *Coming Soon!*