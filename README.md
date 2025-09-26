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

Quote - https://www.goodreads.com/quotes/7630401-code-formatting-is-important-it-is-too-important-to-ignore?utm_source=chatgpt.com
