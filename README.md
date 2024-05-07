# Fraction Class

This Python class, `Fraction`, represents fractions and provides basic arithmetic operations for them.

## Class Structure

- **Initialization**: The class constructor `__init__(self, n=0, d=1)` initializes a fraction with a numerator `n` and a denominator `d`. The default fraction is 0/1.
  
- **String Representation**: The `__str__(self)` method returns a string representation of the fraction in the format "numerator/denominator".
  
- **Arithmetic Operations**:
  - Addition: `__add__(self, other)`
  - Subtraction: `__sub__(self, other)`
  - Multiplication: `__mul__(self, other)`
  - Division: `__truediv__(self, other)`

All these operations are implemented using Python's magic methods.

## Usage

```python
class Fraction:
        
    def __init__(self, n=0, d=1):
        self.num = n
        self.den = d

    def __str__(self):
        return "{}/{}".format(self.num, self.den)

    def __add__(self,other):
        temp_num = self.num * other.den + other.num * self.den
        temp_den = self.den * other.den
        return "{}/{}".format(temp_num,temp_den)

    def __sub__(self,other):
        temp_num = self.num * other.den - other.num * self.den
        temp_den = self.den * other.den
        return "{}/{}".format(temp_num,temp_den)

    def __mul__(self,other):
        temp_num = self.num * other.num
        temp_den = self.den * other.den
        return "{}/{}".format(temp_num,temp_den)
    
    def __truediv__(self,other):
        temp_num = self.num * other.den
        temp_den = self.den * other.num
        return "{}/{}".format(temp_num,temp_den)

# Example usage of the Fraction class
frac1 = Fraction(1, 2)
frac2 = Fraction(3, 4)

# Addition
result_addition = frac1 + frac2  # Result: 5/4

# Subtraction
result_subtraction = frac1 - frac2  # Result: -1/4

# Multiplication
result_multiplication = frac1 * frac2  # Result: 3/8

# Division
result_division = frac1 / frac2  # Result: 2/3
