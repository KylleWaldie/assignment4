# 322 Assignment (class 4) – Markdown Documentation Assignment
The purpose of this assignment is to compare the formating between the C and Python languages. Formating output is fundemnetal for a language and affects both the readability and the user experience. The apporach of the two languages differs significantly.
>“Code formatting is important. It is too important to ignore and it is too important to treat religiously. Code formatting is about communication, and communication is the professional developer’s first order of business.”
>— Robert C. Martin, Clean Code

## Integer Formating
### C99 printf
```
#include <stdio.h>

int main()
{
    int n = 42;
    printf("%5d\n", n);     // width 5, right-alignd
    printf("%+5d\n", n);    // width 5, show sign
    printf("%05d\n", n);    // width 5, pad with zeros
    return 0;
}

Output:
   42
  +42
00042
```
### Python print
```
old-style % formating

n = 42
print("5d" % n)     # width 5, right-aligned
print("+5d" % n)    # width 5, show sign
print("05d" % n)    # width 5, pad with zeros

F-string

print(f"{n:5}")     # width 5, right-aligned
print(f"{n:+5}")    # width 5, show sign
print(f"{n:05}")    # width 5, pad with zeros

output:
   42
  +42
00042
```
## Float Formating
### C99 printf
```
#include <stdio.h>

int main()
{
    float f = 3.14159;
    printf("%8.2f\n", f);   // width 8, 2 decimals
    printf("%08.2f\n", f);  // pad with zeros
    printf("%e\n", f);      // scientific notation
    return 0;
}

Output:
    3.14
00003.14
3.141590e+00
```
## Python
```
old-style % formating

f = 3.14159
print("%8.2f" % f)
print("%08.2f" % f)
print("%e" % f)

F-strings
f = 3.14159
print(f"{f:8.2f}")
print(f"{f:08.2f}")
print(f"{f:e}")

Output:
    3.14
00003.14
3.141590e+00

```

## String Format
### C99 printf
```
#include <stdio.h>

int main() {
    char *s = "Hello";
    printf("%-10s!\n", s); // left-aligned, width 10
    printf("%10s!\n", s); // right-aligned, width 10
    return 0;
}

Output:

Hello     !
     Hello!
```
## Python
```
old-style % formating

s = "Hello"
print("%-10s!" % s)
print("%10s!" % s)

F-strings
s = "Hello"
print(f"{s:<10}!")
print(f"{s:>10}!")
print(f"{s:^10}!")

Output:
Hello     !
     Hello!
  Hello   !
```
------------------------------------------------------------
| Type | Example Code (C) | Example Code (python) | Output
|----------|:--------:|---------:|-------:|
| int  | printf("%5d", 42);  | "%5d" % 42  | 42
| int  | printf("%+5d", 42);  | "%+5d" % 42  |+42
| int  | printf("%05d", 42);  | "%05d" % 42  | 00042
| float  | printf("%8.2f", 3.14159);  | "%8.2f" % 3.14159  | 3.14
| float  | printf("%e", 3.14159);  | "%e" % 3.14159  | 3.141590e+00
| string  | printf("%-10s!", "Hello");  | "%-10s" % "Hello"  | Hello !
| string  | printf("%10s!", "Hello");  | "%10s" % "Hello"  | Hello!

-----

[Python f-strings]https://docs.python.org/3/reference/lexical_analysis.html#f-strings

[C99 printf reference]https://en.cppreference.com/w/c/io/fprintf

[Python old-style % formatting]https://docs.python.org/3/library/stdtypes.html#printf-style-string-formatting

![Logo](https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png)
