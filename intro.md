# Intro

These lines of code should be in all of the programs that you write:

```
#include <stdio.h>
int main(){
   return 0;
}
```

Each statement ends with ;

## Variables

Variables can be declared in this way: (can be initialized or not)
Multiple variables can be declared in the same line, as shown in line 3:

```
int i;
int j = 0;
int x, y;

```

Variable names can include Underscore, Numbers or Alphabet but numbers should not be in the beginning and variable names are case sensitive. Also reserved names can not be used as variable names for example for, if, main, switch are not allowed.
some variable names that are correct:

```
int a;
int A;
int a_b;
int b2;
```

wrong variable names:

```
int 2a;
int a-b-c;
```

It is wrong to use variables before declaring them:

```
printf("%d",a);
int a = 0;
```

 It is wrong to access the value of variable before assigning a value to it

```
int a;
printf("%d",a);
a = 8;
```

## Basic Datatypes
- int: integer
- float: decimal numbers
- double: big decimal numbers and higher percision
- char: characters

```
int a = 1;
float b = 2;
double d = 3.34f;
char c = 'r';

```

If you assign a decimal number to int only the integer part will be assigned to the variable:
```
int x = 3.2;
printf("%d",x);
```

```
3
```

If you assign an integer number to float:
```
float y = 3;
printf("%d",x);
```

```
3.000000
```

