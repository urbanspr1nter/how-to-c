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

