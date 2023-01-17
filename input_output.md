## Input Output
To display a text we use printf function:
```
printf("only text\n");
```
Add these character combinations inside the string inside the printf to show different data types:
- %d: int
- %f: float
- %lf: double
- %c: character

```
int a;
int i = 20;
float f = 23.223f;
double d = 45.1321312321;
char c = 'g';

printf("text inculding integer: %d\n",i);
printf("text inculding float: %f\n",f);     
printf("text inculding double: %lf\n",d);
printf("text inculding character: %c\n",c);
printf("text inculding integer and float: %d, %f\n",i,f);
```
output:
```
text inculding integer: 32767
text inculding integer: 20
text inculding float: 23.223000
text inculding double: 45.132131
text inculding character: g
text inculding integer and float: 20, 23.223000
```

You can format the output by writing in this format % (`%m.pX`)
- m: minimum length
- p: number of digits after decimal point
- X: type of the variable `f` or `lf`

```
printf("%4d\n",i);
printf("%.2f\n",f);
printf("%8f\n",f);
printf("%8.4f\n",f);
```
output:
```
  20
23.22
23.223000
 23.2230
```
### escape characters
- `\n`: next line
- `\t`: tab
- `\"`: "
- `\\`: \

```
printf("before:\n after\n");
printf("before:\t after\n");
printf("before:\" after\n");
printf("before:\\ after");
```
output:
```
before:
 after
before:  after
before:" after
before:\ after
```