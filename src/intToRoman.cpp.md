## Table of Contents  📖

- [Overview](#overview)
- [Prerequisites](#prerequisites)
- [Example Usage](#example-usage)
- [Method Description](#method-description)
  - [Logic and Algorithms](#logic-and-algorithms)
  - [Parameters](#parameters)
  - [Return Values](#return-values)
  - [Complexity Analysis](#complexity-analysis)
- [Implementation Details](#implementation-details)
- [Additional Notes](#additional-notes)

### Overview  🔎

This class provides a function, `intToRoman`, that converts an integer to its roman numeral representation. The roman numeral representation of a number is obtained by combining the appropriate roman numerals for each digit in the number.

### Prerequisites  📚

Before using this class, ensure you have a basic understanding of:
- Roman numerals
- Integer types

### Example Usage  💻

```cpp
int num = 1994;
string romanNumeral = intToRoman(num); // "MCMXCIV"
```

### Method Description  📝

#### Logic and Algorithms 🧮

The `intToRoman` function works by iteratively dividing the number by 1000, 100, 10, and 1, and then using the corresponding roman numeral arrays to append the respective roman numerals to the result string.

#### Parameters 📥

- `num`: The integer to be converted to its roman numeral representation.

#### Return Values 📤

- The roman numeral representation of the input integer.

#### Complexity Analysis ⚖️

The time complexity of the `intToRoman` function is O(1). This is because the length of the roman numeral representation of an integer is bounded by a constant.

### Implementation Details  🛠️

The `intToRoman` function uses four arrays to store the roman numerals for ones, tens, hundreds, and thousands. The function iteratively divides the number by 1000, 100, 10, and 1, and then uses the corresponding roman numeral arrays to append the respective roman numerals to the result string.

### Additional Notes  💬

- The roman numeral representation of a number is not unique. For example, the number 4 can be represented as "IV" or "IIII".
- The `intToRoman` function uses the "subtractive" notation for roman numerals, where a smaller numeral placed before a larger numeral subtracts its value from the larger numeral. For example, "IV" represents the number 4 as "5 - 1".