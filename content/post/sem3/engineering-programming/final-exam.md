---
title: "Final Exam: Engineering Programming - CS204"
description: By now, you lost all of your sanity
date: 2022-01-06
slug: sem3/engineering-programing/final-exam
<!--image: helena-hertz-wWZzXlDpMog-unsplash.jpg-->
categories:
    - Final Exam
    - CS204
    - 4th Semester
---

# Exam overview
Reread my other post [CS204](../), and keep on prayin.  
Also read the [DISCLAIMER](/disclaimer)!

# Ze Exam
## Section 1 MCQs
This section was Multiple Choice Questions.  
`???` is a choice that I forgot :')
### Which of the following is *NOT* a logical operator?
* `&`
* `&&`
* `||`
* `!`

{{< detail "Show Answer" "&" />}}

### Which of the following transfers control to the calling function?
* `switch`
* `return`
* `goto`
* `???`
{{< detail "Show Answer" "return" />}}

### Which is best suidted to get strings that contain spaces from the users.
* `scanf`
* `printf`
* `puts`
* `gets`
{{< detail "Show Answer" "gets" />}}

### Performs operation then checks condition
* `for`
* `do-while`
* `while`
* `???`
{{< detail "Show Answer" "do-while" />}}

### How  many times does the following code repeat? 

```c
for (i=1; i <=10; i=i-1)
```
* `Forever`
* `Never`
* `1`
* `-`
{{< detail "Show Answer" "Forever" />}}

### What is the order of operations in the following code?
```c
z = x + y * z / 1 % 3 -2
```

* `*%/-+=`
* `*/%+-=`
* `=+*/%-`
* `-%/*+=`
{{< detail "Show Answer" "The second one" />}}

### `strcmp` returns what when the string are equal?
* `1`
* `0`
* `-1`
* `first string`
{{< detail "Show Answer" "0" />}}

### Which of the following isn't an arithmatic operation?
* `!=`
* `/=`
* `+=`
* `%=`
{{< detail "Show Answer" "!=" />}}

### Which of the following is *NOT* a correct use of pointers?
* `int arr[i];`
* `int arr[] = {1, 2 3}`
* `int * char;`
* `int char`
{{< detail "Show Answer" "int char" />}}

### What would you use add two string?
* `strcon`
* `strcmp`
* `strcat`
* `stradd`
{{< detail "Show Answer" "strcat" />}}

### Which of the following is the correct way to declare constants?
* `#define a = b`
* `const char a 'b'`
* `const char a = 'b'`
* `const char`
{{< detail "Show Answer" "`const char  a = 'b'`" />}}

### How do you declare a function
* `return-type func-name (argument type);`
* `return-type func-name (argument type){}`
* `return-type (argument type) func-name;`
* `???`
{{< detail "Show Answer" "I am not sure if it is the one with `;` or `{}`. Either first or second" />}}

### How *NOT* to declare a 2D array?
* `int a[3][] = {{1, 2, 3}, {5, 5, 6}, {6, 7, 8}}`
* `int a[][3] = {{1, 2, 3}, {5, 5, 6}, {6, 7, 8}}`
* `int a[1][3]`
{{< detail "Show Answer" "the first answer" />}}

### What is the output of the following?
```c
char str1[50];
char str1[] = "Hello World";

printf("%s\n", strcpy(str1 ,str2)):
```

* `Hello`
* `Hello World`
* Nothing
* Error
{{< detail "Show Answer" "Not sure, I think 'Hello World' " />}}

### How do you declare a zero Array?
* `int a[5] = {};`
* `int a[5];`
* `int a = 0, b = 0, c = 0;`  
`int array[5] = {a, b, c}`
* All of the Above
{{< detail "Show Answer" "All of the Above" />}}

## Section 2: Output of the program
### Program 1:
What is the output of the following code?
```c
#include <stdio.h>

int add(int a, int b);

int main(){
	int a = 10, b = 20, c;
	c = add(a, b);
	printf("c = %d\n", ++c);
}

int add(int a, int b){
	return (a + (++b);
}
```

{{< detail "Show Answer" "c = 32" />}}

### Program 2
What is the output of the following code?
```c
#include <stdio.h>

int main(){
	int a[5] = {1, 10, 5, 13, 40};
	int i, j, k, m;

	i = ++a[1];
	j = a[1]++;
	k = j++;
	m = a[k++];

	printf("%d %d %d %d", i, j, k, m);
}
```
{{< detail "Show Answer" "11, 12, 12, 192929 (any number)" />}}

## Section 3: Correct The Errors
### Program 1
```c
#include <stdin.h>

int main(){
	int n,i;

	scanf("%f", &n);
	for(i=0; i < 10 + n, i++)
		printf("%d", n);
	return 0;
}
```
	
{{< detail "Show Error 1" "`stdin` should be `stdio`" />}}
{{< detail "Show Error 2" "`scanf` should use `%d` instead of `%f` " />}}
{{< detail "Show Error 3" "in the `for` loop `,` should be `;`" />}}
### Program 2
Correct the program so that it prints "This number is odd" and "This
number is even" for odd and even numbers, respectively.

```c
#include <stdio.h>

int main(){
	int value;
	printf("Please input the number");
	scanf("%d", &value);
	
	switch (value/2){
		case 0: printf("This number is odd");
		case 1: printf("This number is even");
	}
	return 0;
}
```

{{< detail "Show Error 1" "should use `%` instead of `/`" />}}
{{< detail "Show Error 2" "missing break after case 0" />}}
{{< detail "Show Error 3" "missing break after case 1, and YES I know there is no need  for that break, I wasn't able to spot any other Error." />}}

## Section 3: Code 
### Code for a triangle program
Code a program to validate a triangle, a valid triangle has all of its
angles = `180`.  
Example output:

```
Please input 3 angles: 90 45 45
This triangle is valid

Please input 3 angles: 90 90 90 
This triangle is invalid
```

{{< detail "Show Answer" "Code it yourself." />}}



### Code to find the sum of an array
Use pointers to find the sum of the following array by using a
function named `sum` that does the sum.
```c
int a[5] = {1, 2, 3, 4, 8};
```
