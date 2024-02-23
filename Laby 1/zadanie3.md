Zadanie 3 
Kumulowanie się błędów. 
```py
import numpy as np
 
def compute1_64(iter):
    sum = 0
    addend = 1.0/iter
    for i in range(0, iter):
        sum += addend
    return sum
 
 
def compute1_32(iter):
    sum = np.float32(0.0)
    addend = np.float32(1/iter)
    for i in range(0, iter):
        sum += addend
    return sum
 
print("32 bit results")    
print(compute1_32(1024) - 1)
print("{:.2E}".format(compute1_32(1000) - 1))
print("{:.2E}".format(compute1_32(10000) - 1))
print("{:.2E}".format(compute1_32(100000) - 1))
 
print("64 bit results")
print(compute1_64(1024) - 1)
print("{:.2E}".format(compute1_64(1000) - 1))
print("{:.2E}".format(compute1_64(10000) - 1))
print("{:.2E}".format(compute1_64(100000) - 1))
```
Przeanalizuj powyższy przykład,    wypróbuj inne parametry dla funkcji computeOne.  
Oblicz błąd bezwzględny i względny.  
Błędy bezwzględne:  
32 bit:  
- 0.0
- -9.30E-06
- 5.35E-05
- 9.90E-04

64 bit:  
- 0.0
- 6.66E-16
- -9.38E-14
- -1.92E-12

Błędy względne:  
takie same