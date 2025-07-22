# Piscine Reloaded

![42 Badge](https://img.shields.io/badge/42-Piscine_Reloaded-brightgreen)
![C Badge](https://img.shields.io/badge/Language-C-blue)
![Shell Badge](https://img.shields.io/badge/Language-Shell-yellow)
![Status Badge](https://img.shields.io/badge/Status-Completed-success)

## What I Learned

Through this comprehensive review project at 42 School, I reinforced and deepened my understanding of fundamental programming concepts:

- **Shell scripting and Unix commands** - Mastered file manipulation, pattern matching, and system operations
- **C programming fundamentals** - Reinforced functions, loops, conditionals, and variable manipulation
- **Pointer arithmetic and memory management** - Strengthened understanding of memory addresses and indirect access
- **Data structures** - Worked with structures, arrays, and basic data organization
- **String manipulation** - Implemented various string processing algorithms and utilities
- **Memory allocation** - Used dynamic memory allocation with malloc for flexible data structures
- **Function pointers** - Applied advanced C concepts for creating generic, reusable code
- **Makefile creation** - Learned build automation and project compilation management
- **File I/O operations** - Handled reading, writing, and manipulating files at the system level
- **Algorithm implementation** - Developed recursive and iterative solutions for mathematical problems

This project solidified my foundation in C programming and Unix systems, preparing me for more advanced software development challenges.

## About the Project

Piscine Reloaded is a comprehensive review of the C Piscine exercises, designed to refresh and reinforce fundamental programming concepts. The project covers everything from basic shell commands to advanced C programming, including:

- Unix command line operations
- File and directory manipulation
- C function implementation
- Memory management
- Data structures
- Build systems

## Project Structure

The project is organized into 28 exercises covering different aspects of programming:

### Shell Exercises (00-05)
- **ex00**: File and directory creation with specific permissions
- **ex01**: Simple file content creation
- **ex02**: Advanced file searching and cleanup commands
- **ex03**: Shell script for finding .sh files
- **ex04**: MAC address display script
- **ex05**: Special character filename creation

### Basic C Functions (06-11)
- **ex06**: Alphabet display function
- **ex07**: Number display function
- **ex08**: Number sign checking function
- **ex09**: Pointer manipulation
- **ex10**: Variable swapping
- **ex11**: Division and modulo operations

### Mathematical Functions (12-14)
- **ex12**: Iterative factorial calculation
- **ex13**: Recursive factorial calculation
- **ex14**: Square root calculation

### String Manipulation (15-17)
- **ex15**: String display function
- **ex16**: String length calculation
- **ex17**: String comparison function

### Program Creation (18-19)
- **ex18**: Command-line argument display
- **ex19**: Sorted argument display

### Memory Management (20-21)
- **ex20**: String duplication with malloc
- **ex21**: Integer range array creation

### Header Files (22-23)
- **ex22**: Absolute value macro definition
- **ex23**: Point structure definition

### Build Systems (24, 27)
- **ex24**: Library compilation Makefile
- **ex27**: Program compilation with file display utility

### Advanced Functions (25-26)
- **ex25**: Function application to arrays
- **ex26**: Conditional counting function

## Implementation Highlights

### Key Functions Implemented

| Category | Functions | Description |
|----------|-----------|-------------|
| **Basic I/O** | ft_print_alphabet, ft_print_numbers | Character and digit output |
| **Conditionals** | ft_is_negative | Sign checking and branching |
| **Pointers** | ft_ft, ft_swap, ft_div_mod | Memory manipulation and indirect access |
| **Mathematics** | ft_iterative_factorial, ft_recursive_factorial, ft_sqrt | Algorithm implementation |
| **Strings** | ft_putstr, ft_strlen, ft_strcmp, ft_strdup | String processing and manipulation |
| **Memory** | ft_range | Dynamic memory allocation |
| **Function Pointers** | ft_foreach, ft_count_if | Generic programming techniques |

### Shell Scripting Skills

```bash
# Finding and cleaning temporary files
find . -name "*~" -o -name "#*#" -delete

# Extracting filenames without extensions
find . -name "*.sh" -exec basename {} .sh \;

# MAC address extraction
ifconfig | grep ether | awk '{print $2}'
```

### Advanced C Concepts

```c
// Function pointer usage
void ft_foreach(int *tab, int length, void (*f)(int));

// Structure definition
typedef struct s_point {
    int x;
    int y;
} t_point;

// Macro definition
#define ABS(Value) ((Value) < 0 ? -(Value) : (Value))
```

## Technical Challenges Overcome

- **Complex file permissions** - Understanding and implementing specific Unix permission patterns
- **Shell metacharacter handling** - Creating files with special characters in names
- **Recursive algorithms** - Implementing mathematical functions using recursion
- **Memory allocation patterns** - Managing dynamic memory for array creation
- **Function pointer application** - Using callbacks for generic array processing
- **Makefile dependencies** - Creating efficient build systems with proper rule dependencies
- **Error handling** - Implementing robust error checking for file operations and edge cases

## Build Instructions

```bash
# Navigate to project directory
cd C_Piscine_reload

# For exercises with Makefiles (ex24, ex27)
cd ex24
make        # Build library
make clean  # Remove object files
make fclean # Remove all generated files
make re     # Rebuild from scratch

# For individual C files
cc -Wall -Wextra -Werror -o program file.c

# For shell scripts
chmod +x script.sh
./script.sh
```

## Usage Examples

### String Operations
```c
#include "libft.h"

int main(void)
{
    char *str = ft_strdup("Hello, World!");
    ft_putstr(str);
    
    int len = ft_strlen(str);
    printf("Length: %d\n", len);
    
    free(str);
    return (0);
}
```

### Mathematical Functions
```c
int result = ft_recursive_factorial(5);  // Returns 120
int root = ft_sqrt(16);                  // Returns 4
```

### Function Pointers
```c
void print_number(int n) {
    ft_putnbr(n);
    ft_putchar('\n');
}

int numbers[] = {1, 2, 3, 4, 5};
ft_foreach(numbers, 5, &print_number);
```

## Learning Outcomes

This project reinforced essential programming skills:

1. **Code Organization** - Structuring programs with clear function separation
2. **Memory Safety** - Proper allocation and deallocation practices
3. **Algorithm Design** - Implementing both iterative and recursive solutions
4. **System Programming** - Understanding Unix file systems and permissions
5. **Build Automation** - Creating maintainable compilation systems
6. **Generic Programming** - Using function pointers for flexible code design

---

*This project was completed as part of the 42 School curriculum, demonstrating proficiency in C programming fundamentals, Unix system operations, and software engineering practices. The exercises provide a solid foundation for advanced programming concepts and system-level development.*

---

## License

This project is licensed under the [MIT License](./LICENSE).
