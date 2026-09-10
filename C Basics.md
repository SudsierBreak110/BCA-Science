	## Brief History
C is a low level language created by Dennis Ritchie in around 1972 for the UNIX operating system, and is the successor to the B and BCPL programming languages. 

## Execution Steps of a C Program
There are multiple steps have occur before a C program is executed:

1. **Edit** - Refers to writing/editing the C program.
2. **Preprocess** - Refers to resolving the `#include`, `#define` statements.
3. **Compile** - Compiles the source code into object code.
4. **Link** - Links each function call to its definition.
5. **Load** - Loads all the required files needed for execution of the program in the RAM.
6. **Execute** - Executes the file.

> [!abstract]
> ```c
> #include<stdio.h>
> int main(){
> printf("Hello World");
> return 0;
> }
> ```
The `#include` is the preprocessor directive and the `<stdio.h>` is the header file.


> [!info] Note
> - C is a case sensitive language.
> - Every statement in C ends with a semicolon `;`


## <font color="#4bacc6">Datatypes</font>

| <font color="#9bbb59">Datatype</font> | <font color="#9bbb59">Memory required <br>(in bytes)</font><br> |
| ------------------------------------- | --------------------------------------------------------------- |
| char                                  | 1                                                               |
| short                                 | 2                                                               |
| int                                   | 4                                                               |
| long                                  | 4 or 8                                                          |
| float                                 | 4                                                               |
| double                                | 4 or 8                                                          |
| bool                                  | 1 bit ($\tiny{1/8}$ byte)                                       |

## C basics

```c
int a, b, c;
a = 0;
```
- `int a, b, c` is a <font color="#f79646">declaration statement</font>. The compiler creates 3 memory locations of 4 bytes each (as these are integers) and names them `a`, `b` and `c`. Previously these memory locations were <font color="#f79646">not named and were a Hexadecimal address</font>. 
- `a = 0;` is an <font color="#f79646">initialization statement</font>. It is used to remove garbage values and set a variable to a particular value.
- Note every statement terminates with a semicolon.

### <font color="#4bacc6">Format Specifiers</font>


| <font color="#9bbb59">Format Specifiers</font> | <font color="#9bbb59">Data Type</font> | <font color="#9bbb59">Purpose</font>     |
| ---------------------------------------------- | -------------------------------------- | ---------------------------------------- |
| `%d` or `%i`                                   | `int`                                  | Signed decimal integer                   |
| `%u`                                           | `unsigned int`                         | Unsigned decimal integer                 |
| `%f`                                           | `float`                                | Decimal floating point                   |
| `%lf`                                          | `double`                               | Double precision floating point          |
| `%c`                                           | `char`                                 | Single character                         |
| `%s`                                           | `String`                               | Sequence of characters, terminated by \0 |
| `%p`                                           | `void`                                 | Memory address (pointer) in hexadecimal  |
| `%x` or `%X`                                   | `int`                                  | Hexadecimal format                       |
| `%o`                                           | `int`                                  | Octal format                             |
| `%%`                                           | None                                   | Prints the `%` character                 |

### <font color="#4bacc6">Output Formatting</font>

- **Width (`%5d`)**: Defines the minimum number of characters to print. Pads with spaces if the value is shorter

- **Precision (`%.2f`)**: Controls the number of digits shown after the decimal point for floats.

- **Left Alignment (`%-5d`)**: Left-aligns the output within the specified minimum width (defaults to right-aligned).

- **Zero Padding (`%05d`)**: Pads the output field with leading zeros instead of spaces.

## Variable Declaration

##### Variable Name Convention
- Variables do not start with digits.
- Variables do not contain special characters. Underscore `_` is allowed.
- Variable names cannot be keywords.

### Constants

Constant variables and declared with the `const` keyword. The value of these variables **can not** change at runtime.

```c
int main(){
	const int a = 5;
	a += 2;
	printf("%d", a);
}
```
> [!error]
> error: assignment of read-only variable 'a'.
> 
> The above code throws and error as we tried to change the value of the constant at runtime

## Arithmetic Operators

| <center><font color="#9bbb59">Operator</font></center> | <center><font color="#9bbb59">Function</font></center> |
| ------------------------------------------------------ | ------------------------------------------------------ |
| <center>`+`</center>                                   | <center>Addition</center>                              |
| <center>`-`</center>                                   | <center>Subtraction</center>                           |
| <center>`*`</center>                                   | <center>Multiplication</center>                        |
| <center>`/`</center>                                   | <center>Division (Quotient)</center>                   |
| <center>`%`</center>                                   | <center>Division (Remainder)</center>                  |

## Relational Operators

| <center><font color="#9bbb59">Operator</font></center> | <center><font color="#9bbb59">Function</font></center> |
| ------------------------------------------------------ | ------------------------------------------------------ |
| <center>`>`</center>                                   | <center>Greater than</center>                          |
| <center>`<`</center>                                   | <center>Less than</center>                             |
| <center>`>=`</center>                                  | <center>Greater than or equal to</center>              |
| <center>`<=`</center>                                  | <center>Less than or equal to</center>                 |
| <center>`==`</center>                                  | <center>Equal to</center>                              |
| <center>`!=`</center>                                  | <center>Not equal to</center>                          |

### Conditional / Ternary Operator

This operator operates on 3 values.

> [!example] Syntax
> ```c
>condition ? expression1 : expression2;
>```
>If the `condition` is true, `expression1` is evaluated, else `expression2` is evaluated. 
>

## Unary Operators

There are 2 unary operators: `++` and `--`. These operators increment and decrement the variable respectively. They can be either used before or after the variable.

```c
int x = 2;
printf("%d", x);
printf("\n%d", x++);
printf("\n%d", x);
```
> [!done] Output
> 2
> 2
> 3

Post-incrementing prints the value before incrementing.


```c
int x = 2;
printf("%d", x);
printf("\n%d", ++x);
printf("\n%d", x);
```
> [!done] Output
> 2
> 3
> 3

Pre-incrementing prints the value after incrementing.


## Logical Operators
  
| <center><font color="#9bbb59">Operator</font></center> | <center><font color="#9bbb59">Function</font></center> |
| ------------------------------------------------------ | ------------------------------------------------------ |
| <center>`&&`</center>                                  | <center>Logical AND</center>                           |
| <center>\|\|</center>                                  | <center>Logical OR</center>                            |
| <center>`!`</center>                                   | <center>Logical NOT</center>                           |


## Bitwise Operators
  
| <center><font color="#9bbb59">Operator</font></center> | <center><font color="#9bbb59">Function</font></center> |
| ------------------------------------------------------ | ------------------------------------------------------ |
| <center>`&`</center>                                   | <center>Bitwise AND</center>                           |
| <center>\|</center>                                    | <center>Bitwise Inclusive OR</center>                  |
| <center>`^`</center>                                   | <center>Bitwise Exclusive OR</center>                  |
| <center>`~`</center>                                   | <center>Bitwise NOT</center>                           |
| <center>`<<`</center>                                  | <center>Shifts bits to the left</center>               |
| <center>`>>`</center>                                  | <center>Shifts bits to the right</center>              |

## Decision Control Statements
- `if ... else`
- `switch ... case`

### if else

This statement is used when we want to execute block of statements if a certain condition is true, else it executes a different set of statements.

> [!example] Syntax
> ```c
> if(condition){
> 	statements;
> }else{
> 	statements;
> }
> ```
```c
if(a < b){
	printf("%d", a); // executes if a < b is true
}else{
	printf("%d", b); // executes if a < b is false
}
```

The `if else if` statement is another variant of the `if else` statement, which can has multiple conditions.

```c
if(marks >= 75){
	printf("Decent score");
}else if (marks >= 50){
	printf("Barely passed");
}else{
	printf("Failed");
}
```

### switch case

The `switch` statement provides a better way of writing when comparing an expression with multiple constant values, instead of writing long `if else if` ladders.

>[!example] Syntax
>```c
>switch(expression){
>	case constant_1:
>		statements;
>		break;
>		
>	case constant_2:
>		statemnets;
>		break;
>	 .
>	 .
>	 .
>	case constant_n:
>		 statements;
>		 break;
>	 
>	default:
>		 statements;
>}
>```
>
>This block compares the `expression` with the `case` constants and executes the block where the `expression` matches the `case`. If nothing matches, the `default` case is executed.
>
>The `break` is required, or else the execution "Falls Through" subsequent cases and their code will be executed regardless of whether the cases match or not.

```c
char grade = 'B';

switch (grade){
	case 'A':
		printf("Excellent!\n");
		break;
		
	case 'B':
		printf("Well done!\n"); // This block will execute
		break;
		
	case 'C':
		printf("You passed.\n");
		break;
		
	default:
		printf("Invalid grade.\n");
} 
```
