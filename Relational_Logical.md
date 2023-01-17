# Relational and Logical Operators

## Relational Operators

- `<`: less than
- `>`: greater than
- `<=`: less than or equal to
- `>=`: greater than or equal to

These operators produce 0 (false) or 1 (true):

```C
printf("%d\n",(2>3));
printf("%d\n",(2<=3));
```

Output:

```C
0
1
```

Operands of mixed types can be used with relational operators for example one operand can be integer and the other one can be float:

```C
printf("%d\n",(2>3.6));
```

Output:

```Console
0
```

Precedence of relational operator is lower than arithmetic operators:

```C
i+j < k-1;
```

is equal to:

```C
(i+j) < (k-1);
```

Relational operators is are left associative:

```C
i<j<k
```

is same as:

```C
(i<j)<k
```

and it is different from:

```C
(i<j) && (j<k)
```

## Equality Operators

Equality operators are left associative (evaluate from left to right) and produce either 0 (false) and 1 (true)

- `==`: equal to
- `!=`: not equal to

Equality Operators have lower precedence than relational operators:

```C
i<j == i<k
```

is same as:

```C
(i<j)==(i<k)
```

## Logical Operators

- `!`: negation
- `&&`: and
- `||`: or

`!` is unary operator while `&&` and `||` are binary
They all produce 0 or 1

They treat any non zero operand as true (1)

|     | 0 | 1 |
| ----- | --- | --- |
| `!` | 1 | 0 |

| `&&` | 0 | 1 |
| ------ | --- | --- |
| 0    | 0 | 0 |
| 1    | 0 | 1 |

| or | 0 | 1 |
| ---- | --- | --- |
| 0  | 0 | 1 |
| 1  | 1 | 1 |

### Short-Circuit Nature of `&&` and `||`

Side effects in logical expressions may not ocurr.

```C
i > 0 && ++j > 0
```

If `i>0` is false it will not check `++j>0` because there is no need to evaluate the second statement, so value of j will not change.

The `!` has the same precedence as the unary plus and minus operators.
The precedence of `&&` and `||` is lower than that of the relational and equality operators.
`!` is right associative. `&&` and `||` are left associative (evaluate from left to right)

### Precedence

- Arithmetic:
  - `++i`,`--i`
- Unary: `!i`, `+i`, `-i`
- Arithmetic:
  - `i/j`, `i*j`, `%`
  - `i+j`, `i-j`
- Relational:
  - `i<j`, `i>j`, `i<=j`,`i>=j`
- Equality:
  - `i!=j`, `i==j`
- Assignment:
  - `=`,`*=`, `/=`, `+=`, `-=`
