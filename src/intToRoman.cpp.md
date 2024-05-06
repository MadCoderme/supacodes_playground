**Table of Contents**

- [Introduction](#introduction)
- [Code Explanation](#code-explanation)
- [Example Usage](#example-usage)
- [Additional Information](#additional-information)
- [Links](#links)

**Introduction**

The provided code is a C++ implementation of the `intToRoman()` function, which converts an integer into its Roman numeral representation. Roman numerals are a system of numerical notation used in ancient Rome, where numbers are represented by combinations of letters.

**Code Explanation**

The function utilizes four helper string arrays:

- `ones`: Stores Roman numerals for numbers 1 to 9
- `tens`: Stores Roman numerals for numbers 10 to 90
- `hrns`: Stores Roman numerals for numbers 100 to 900
- `ths`: Stores Roman numerals for numbers 1000 to 3000

The function operates as follows:

1. It calculates the thousands digit of the input number and retrieves the corresponding Roman numeral from the `ths` array.

2. It then calculates the hundreds digit of the remaining number and retrieves the corresponding Roman numeral from the `hrns` array.

3. Next, it calculates the tens digit of the remaining number and retrieves the corresponding Roman numeral from the `tens` array.

4. Finally, it calculates the ones digit of the remaining number and retrieves the corresponding Roman numeral from the `ones` array.

5. It concatenates the retrieved Roman numerals in descending order to form the final result.

**Example Usage**

Example code
```cpp
#include <iostream>

using namespace std;

int main() {
  int num = 1994;
  string romanNumeral = intToRoman(num);
  cout << "The Roman numeral representation of " << num << " is: " << romanNumeral << endl;
  return 0;
}
```

Output:

﻿```
The Roman numeral representation of 1994 is: MCMXCIV
﻿```

**Additional Information**

- Roman numerals do not use the digits 0 or negative numbers.
- The values represented by Roman numerals are additive, meaning that the values of the individual symbols are added together to determine the overall value.
- The symbols are always written in descending order of value, with the exception of IV and IX, which are used to represent 4 and 9, respectively.

**Links**

- [Roman Numerals](https://en.wikipedia.org/wiki/Roman_numerals)
- [C++ Strings](https://www.cplusplus.com/reference/string/string/)
