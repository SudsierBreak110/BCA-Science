## <font color="#4bacc6">Bases</font>
Number systems are distinguished from each other using bases. The base of a number system is the  number of unique symbols it has. For example, decimal has 10 unique symbols (0 - 9), binary has 2 (0 and 1).

---
- **Decimal System** 
	Base - 10
	(0, 1, 2, 3, 4, 5, 6, 7, 8, 9)
- **Binary System** 
	Base - 2
	(0, 1)
- **Octal System**
	Base - 8
	(0, 1, 2, 3, 4, 5, 6, 7)
- **Hexadecimal System**
	Base - 16
	(0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, F)

## <font color="#4bacc6">Conversions</font>

### Decimal to others
To convert a decimal number to a number system having a different base (2, 8, 16), <font color="#f79646">divide the number by the base repeatedly</font> until it cannot be divided any further. <font color="#f79646">Note the remainder</font> on each step. Write the <font color="#f79646">remainders in reverse order</font> to obtain the converted number.

Example: To convert (1000)<sub>10</sub> to base 2:

| <font color="#9bbb59">Base</font> | <font color="#9bbb59">Number</font> | <font color="#9bbb59">Remainder</font> |
| --------------------------------- | ----------------------------------- | -------------------------------------- |
| 2                                 | 1000                                |                                        |
| 2                                 | 500                                 | 0                                      |
| 2                                 | 250                                 | 0                                      |
| 2                                 | 125                                 | 0                                      |
| 2                                 | 62                                  | 1                                      |
| 2                                 | 31                                  | 0                                      |
| 2                                 | 15                                  | 1                                      |
| 2                                 | 7                                   | 1                                      |
| 2                                 | 3                                   | 1                                      |
|                                   | 1                                   | 1                                      |
We get the remainders 0001011111. By reversing it we get 1111101000

(1000)<sub>10</sub> = (1111101000)<sub>2</sub> 

### Binary to Hexadecimal
Separate the binary number into <font color="#f79646">groups of four starting from the right.</font> Add zeros on the left side if there are less than four left. Convert the groups of four to Hexadecimal.

Example: To convert (10011011101)<sub>2</sub> to Hexadecimal

0100 | 1101 | 1101 --> 4 | 13 | 13 --> 4CC

(10011011101)<sub>2</sub> = (4CC)<sub>16</sub>

### Binary to Octal
Separate the binary number into <font color="#f79646">groups of three starting from the right.</font> Add zeros on the left side if there are less than four left. Convert the groups of three to Octal.

Example: To convert (10011011101)<sub>2</sub> to Octal

010 | 011 | 011 | 101 --> 2 | 3 | 3 | 5 --> 2335

(10011011101)<sub>2</sub> = (2335)<sub>8</sub>

### Hexadecimal/Octal to Binary
<font color="#f79646">Take each digit of the number and convert it to binary </font>(3 digits for Octal, 4 digits for Hexa).

**Example 1:** (61A)<sub>16</sub> to Binary

6 | 1 | A --> 0110 | 0001 | 1010 --> 011000011010

(61A)<sub>16</sub> = (011000011010)<sub>2</sub>


**Example 2:** (721)<sub>8</sub> to Binary

7 | 2 | 1 --> 111 | 010  | 001 --> 111010001

(721)<sub>8</sub> = (111010001)<sub>2</sub>

### Hexadecimal to Octal/ Vice versa
Convert the Hexadecimal to <font color="#f79646">binary first</font> then convert the binary to Octal and vice versa.

## <font color="#4bacc6">Operations </font>

### Addition
- 0 + 0 = 0
- 1 + 0 = 1
- 0 + 1 = 1
- 1 + 1 = 10 (0, carry 1)

### Subtraction
- 0 - 0 = 0
- 1 - 0 = 1
- 1 - 1 = 0 
- 0 - 1 = 11 (1, borrow 1)

> [!tip] How to Borrow
> Substract normally first and subtract the borrowed bit from it after.

### Multiplication
- 0 x 0 = 0
- 1 x 0 = 0
- 0 x 1 = 0
- 1 x 1 = 1

<font color="#f79646">Multiplication in binary is the same as it is for decimal.</font>

### Division

<font color="#f79646">Division in binary is the same as it is for decimal.</font>


## <font color="#4bacc6">Floating point Decimal to Binary</font>

The floating point decimal can be split into 2 parts: the integer part and the fractional part. The <font color="#f79646">integer part is calculated the same way as mentioned above.</font> 

To convert the fractional part:

1. Take the<font color="#f79646"> fractional part and multiply it by 2</font>. Note the leading integer (the digit before the`.`)

2. Repeat until the fractional part either:
	- Becomes 0
	- repeats

3. Write the <font color="#f79646">leading digits from top to bottom</font>. This gives us the binary number for the fractional part.
	Eg - 0.625 to binary.
	
	**0.625 × 2 = 1.25 → 1**  
	**0.25 × 2 = 0.5 → 0**  
	**0.5 × 2 = 1.0 → 1**        we stop here as the fractional value became `0`.


## Gray Code

In this number system, each number is represented by only changing a singular bit from the previous number. This is used in systems which can only modify one bit at a time.

To convert Binary to Gray Code, we keep the MSB (Most Significant Bit, aka the leftmost bit) as it is.


