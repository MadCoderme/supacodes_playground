## 📑 Table of Contents

* [`intToRoman` Function](#inttoroman-function)


## ➡️ `intToRoman` Function

The `intToRoman` function converts an integer `num` into its corresponding Roman numeral representation.

### 📋 Function Signature

```cpp
string intToRoman(int num);
```

### 🔨 Implementation Details

The function utilizes pre-defined arrays to represent Roman numeral symbols for different桁位:

* `ones`:   Units (I - IX)
* `tens`:   Tens (X - XC)
* `hrns`:  Hundreds (C - CM)
* `ths`:    Thousands (M - MMM)

The function calculates the Roman numeral representation by:

1. Extracting the thousands digit (`num / 1000`) and appending the corresponding symbol from the `ths` array.
2. Extracting the hundreds digit (`(num % 1000) / 100`) and appending the corresponding symbol from the `hrns` array.
3. Extracting the tens digit (`(num % 100) / 10`) and appending the corresponding symbol from the `tens` array.
4. Extracting the ones digit (`num % 10`) and appending the corresponding symbol from the `ones` array.

### ➡️ Return Value

The function returns a string representing the Roman numeral equivalent of the input integer `num`.