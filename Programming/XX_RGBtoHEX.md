# Quick Reference
- https://www.educative.io/answers/rgb-to-hex

## [RGB color codes](https://www.educative.io/answers/rgb-to-hex#:~:text=RGB%20to%20Hex-,RGB%20color%20codes,-RGB%20color%20codes)

**RGB color codes** are one of the most popular ways to define colors in web pages. They are written in the following way:

```
color: rgb(0, 0, 0);       /* black */
color: rgb(255, 255, 255); /* white */
```

## [Hex color codes](https://www.educative.io/answers/rgb-to-hex#:~:text=%3B%20/*%20white%20*/-,Hex%20color%20codes,-Hex%20color%20codes)

**Hex color codes** use the same principle as RGB color codes, as they both define colors using the RGB color mode. However, they are written in a slightly different way:

color: #000000; /* black */
color: #FFFFFF; /* white */

## [Converting Hex to RGB color codes](https://www.educative.io/answers/rgb-to-hex#:~:text=Converting%20Hex%20to%20RGB%20color%20codes)

RGB color code values are based on the decimal number system, which is a Base-10[^1] system.

Hex color code values are based on the hexadecimal number system. It is a Base-16 system, meaning there are 16 unique characters that define the numbers. This includes the numbers `0 – 9` and the letters `A – F`.

## [How counting is done](https://www.educative.io/answers/rgb-to-hex#:~:text=How%20counting%20is%20done)

Counting is done the same way in both systems. The first number is 0, and you count all the way up to the last digit. For the decimal number system, this digit is 9. For the hexadecimal number system, this digit is F.

Once you reach the last digit, you start the count again, but this time with your leading digit as the next one in the system[^2].

Below is a chart that helps to show the difference in the two number systems:

<img width="884" height="222" alt="image" src="https://github.com/user-attachments/assets/8f5587fd-78c0-4372-97b5-21397dda2b23" />

In order to convert an RGB color code to a hex color code, you must convert each of the values individually.

## [Example](https://www.educative.io/answers/rgb-to-hex#:~:text=the%20values%20individually.-,Example,-Let%E2%80%99s%20look%20at)

Let’s look at the color `crimson` as an example. The RGB color code for crimson is `rgb(220, 20, 60)`.

### First Value

- Take the first number, 220, and divide by 16.
  `220 / 16 = 13.75`
  > This means that the first digit of the 6-digit hex color code is 13 or D.
- Take the `remainder` of the first digit, 0.75, and multiply by 16.
  `0.75 (16) = 12`
  > This means that the second digit of the 6-digit hex color code is 12, or C.
  So far, we have `#DC____`.
  
### Second Value

- Take the second number, 20, and divide by 16.
  `20 / 16 = 1.25`
  > This means that the third digit of the 6-digit hex color code is 1.
- Take the remainder of the first digit, 0.25, and multiply by 16.
  `0.25 (16) = 4`
  > This means that the fourth digit of the 6-digit hex color code is 4.
  In addition to what we already had, we now have `#DC14__`.

### Third Value

- Take the third number, 60, and divide by 16.
  `60 / 16 = 3.75`
  > This means that the fifth digit of the 6-digit hex color code is 3.
- Take the remainder of the first digit, 0.75, and multiply by 16.
  `0.75 (16) = 12`
  > This means that the sixth digit of the 6-digit hex color code is 12, or C.
  Finally, we have our total value of `#DC143C`.

[^1]: this means that there are 10 unique characters that define the numbers 0 – 9
[^2]: 1 for both the decimal and hexadecimal number systems
