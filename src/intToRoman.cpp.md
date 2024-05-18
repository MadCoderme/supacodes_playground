## 📑 Solution Class

### 📋 Table of Contents

* 👉 Overview
* ➡️ `intToRoman` Function

### 👉 Overview

The code defines a `Solution` class containing a single function, `intToRoman`, for converting integers to their Roman numeral representations.

### ➡️ `intToRoman` Function

**SYNOPSIS**

```cpp
string intToRoman(int num);
```

**DESCRIPTION**

The `intToRoman` function converts an integer `num` into its corresponding Roman numeral representation and returns it as a string.

**PARAMETERS**

* `num`: An integer representing the number to be converted.

**RETURN VALUE**

A string representing the Roman numeral equivalent of the input integer.

**IMPLEMENTATION DETAILS**

1. **Predefined Arrays for Roman Numerals:**

    * `ones`: Stores Roman numerals for numbers 1 to 9.
    * `tens`: Stores Roman numerals for multiples of 10 from 10 to 90.
    * `hrns`: Stores Roman numerals for multiples of 100 from 100 to 900.
    * `ths`: Stores Roman numerals for thousands (1000, 2000, 3000).

2. **Integer Decomposition and Concatenation:**

    * The function calculates the thousands, hundreds, tens, and ones components of `num` using modulo arithmetic.
    * It then concatenates the corresponding Roman numeral strings from the predefined arrays to form the complete Roman numeral representation.

```cpp
        return ths[num/1000] + hrns[(num%1000)/100] + tens[(num%100)/10] + ones[num%10];
```