Zadanie 2  
Błąd obcięcia w praktyce. Nie należy stosować   bezpośredniego porównania dla liczb zmiennoprzecinkowych. 
```py
a = np.float32(0.1)
b = np.float32(0.2)
 
print(0.1 + 0.2 == 0.3)      # Wrong! Do not compare floating point numbers like this
print(a + b - np.float32(0.2))
```
Przeanalizuj powyższy przykład. Skąd bierze się błąd obliczeń?

- Błąd obliczeń bierze się ze skończonej liczby bitów używanych do zapisania ułamka, które zostają zaokrąglone.