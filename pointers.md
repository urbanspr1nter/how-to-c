# Pointers

## Examples

### Ex. 1

What is the output of `x`?

```c
int *x;
int y = 3;

x = &y;

printf("%d\n", *x);
```

### Ex. 2

How would I update `x` to be 5? Follow up, what is the address of `x`? What is the address of `y`? If you were to print `y`, what do you get now? Why is that?

```c
int y = 3;
int *x = &y;

printf("%d\n", *x);

// ??? Update code ???

printf("%d\n", *x);
```

### Ex. 3

How would I assign `z` to be the same address as `x`? Be very careful about this one, and try to notice the types. 

If `z` and `x` are the same address, can I use `*z` to get the value of `y`? Write a print statement to confirm this.

```c
int y = 8;
int *x = &y;
int *z;

// ??? Update code ???

printf("%p, %p. Are they the same address? %d\n", z, x, z == x);
```

### Ex. 4

How do I pass in the `x` to this function? We want to increment the value `x` by 1, but also have this value be reflected _outside_ of the `do_something` function. How do we accomplish this?

```c
void do_something(/* your code here */) {
    // Increment x by 1 here.
}

int main(void) {
    int x = 5;

    // call do something

    printf("%d\n", x);
}
```

### Ex. 5

Iterate through the array of `int` - Can you not use array subscripting and instead dereference the elements at the address offset to print out the value?

Can you answer this question now: Are array subscripts and pointer dereferencing the same? 

```c
void print_data(int* data, int num_elements) {
    for (int i = 0; i < num_elements; i++) {
        printf("%d\n", /* complete this */);
    }
}

int main(void) {
    int d[5] = {4, 5, 2, 9, 9};

    print_data(/* complete this */);

    return 0;
}
```

### Ex. 6 

Given a `struct` with this declaration:

```c
struct Dog {
    char name[10];
    int age;
};
```

How do I complete this code? Please note that `struct` are value types, so they are just like any other data type. So we can pass them as pointers too just like `int`, `char`, etc.

```c
void print_info(struct Dog* d) {
    char* name = // ... Complete this

    printf("The dog's name is: %s\n", name);
    printf("The dog's age is: %d\n", /* ... Complete this */);
}

int main(void) {
    struct Dog d = {.name = "Bill", .age = 4};
    print_info(/* Complete this */); // Hint: Reference the struct. What operator is this?

    return 0;
}
```

### Ex. 7

Write a function to find the length of a string. You cannot use `strlen`. Remember `char*` are strings that end with a `\0' character.

```c
int find_string_length(char* str) {
    /* complete this */
}

int main(void) {
    char* h = "hello, world";

    int length = find_string_length(/* complete this */);

    printf("The length of the string is: %d\n", length);

    return 0;
}

```