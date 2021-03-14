# NumeralSystemConverter

# Description

Fractional numbers can also be converted from one base to another. To convert a fractional number to another base, you should use the algorithm described below.

# Algorithm

As you know from the previous stage, in order to convert a number from one base to another, first, we need to convert it to decimal if it’s not decimal yet, and only then convert it to another base. The same applies to fractional numbers.

Let’s imagine you have a fractional number ab.cdef where ab is the integer part, cdef is the fractional part, and a,b,c,d,e,f are some digits or letters, depending on the base of the number.

In this case, we have 2 digits (letters) in the integer part and 4 digits (letters) in the fractional part. In other cases, the number of digits (letters) in parts can be different.

To convert the number into decimal, we need to:

* Split the number into two parts: integer and fractional;
* Convert the integer part into decimal using the method from the previous stage;
* Convert the fractional part into decimal using the following formula:

![image](https://user-images.githubusercontent.com/59764846/111079654-235eb880-84fb-11eb-95e1-070af75e84a4.png)

where base is a base of the number you want to convert into decimal.

The more digits (letters) in the fractional part, the more addends in the formula. If the fractional part has letters, then you should use their number representation: ‘a’ – 10, ‘b’ – 11, c – ‘12’, and so on.

As a result, you should get a decimal number no greater than 1. If it is greater than 1, you did something wrong.

To see the decimal representation of the source number, you can sum the decimal integer and the decimal fractional parts.

To convert a decimal fractional number into any other base, we need to:

* Split the decimal number into two parts: integer and fractional;
* Convert the integer part into the new base;
* Convert the fractional part from decimal to any other base.
* Let’s elaborate on the third step and convert the fractional part of 0.5168 into base 19 as an example.

Multiply the fractional part by the new base: 0.5168∗19=9.8192
0.5168 ∗ 19= 9.8192.The integer part of the result is the first digit (or letter if the integer part is greater than 9) in the fractional part of a number in the new base. In this case, the first digit in the fractional part is 9.

Take the fractional part from the result of the multiplication and multiply it by the new base again: 0.8192∗19=15.5648
0.8192 ∗ 19 = 15.5648. For numbers greater than 9, you should use their letter representation: 10 – ‘a’, 11 – ‘b’, 12 – ‘c’, and so on. In this case, the second digit (letter) is f (15).

To calculate the rest of the digits (letters), you should repeat this action. In this stage, your program should output only 5 digits (letters) in the fractional part:

![image](https://user-images.githubusercontent.com/59764846/111079711-73d61600-84fb-11eb-893b-643bfed64c76.png)

The final result looks like this:  0.5168₁₀=0.9fadg₁₉
