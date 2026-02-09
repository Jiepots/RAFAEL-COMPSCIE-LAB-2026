# Computer Lab - Pi Truncation vs Rounding


## What This Program Does

This lab assignment asked us to:
- Find a formula using pi (not just circle stuff)
- Compare truncation vs rounding at 20, 40, 60, and 100 decimal places
- See if there's actually a difference

## The Formulas I Used

I found two cool formulas that use pi but aren't circle formulas:

### 1. Bailey-Borwein-Plouffe (BBP) Formula
```
π = Σ[1/16^k * (4/(8k+1) - 2/(8k+4) - 1/(8k+5) - 1/(8k+6))]
```
This one's pretty interesting because you can calculate any digit of pi without knowing the ones before it!

### 2. Machin's Formula
```
π = 16*arctan(1/5) - 4*arctan(1/239)
```
This was actually used to calculate pi to hundreds of digits back in the day.

## What I Used
- Python 3
- mpmath library (for high precision)

## Results

Here's what I found:

### At 20 Decimal Places
```
Truncated: 3.1415926535897936
Rounded:   3.141592653589793
→ Different values!
```

### At 40, 60, and 100 Decimal Places
```
Truncated: 3.141592653589793
Rounded:   3.141592653589793
→ Same value
```

## My Conclusion

**Yes, there IS a difference!**

At 20 decimals you can see it clearly - truncation just chops off the number while rounding actually gives you a more accurate value. At higher decimal places they end up the same because of how computers store numbers.

So basically, if you want accurate calculations, use rounding instead of truncation.

## How to Run

1. Install mpmath:
```bash
pip install mpmath
```

2. Run the program:
```bash
python3 pi_lab.py
```

## Output Screenshot

```
======================================================================
COMPUTER LAB: Pi Truncation vs Rounding
======================================================================

Formulas using pi (NOT circle formulas):

1. Bailey-Borwein-Plouffe Formula:
   π = Σ[1/16^k * (4/(8k+1) - 2/(8k+4) - 1/(8k+5) - 1/(8k+6))]
   Result: 3.14159265358979323846264338327950288...

2. Machin's Formula:
   π = 16*arctan(1/5) - 4*arctan(1/239)
   Result: 3.14159265358979323846264338327950288...

======================================================================
COMPARISON: Truncation vs Rounding
======================================================================

--- At 20 decimal places ---
Truncated: 3.1415926535897936
Rounded:   3.141592653589793
→ Different values!
