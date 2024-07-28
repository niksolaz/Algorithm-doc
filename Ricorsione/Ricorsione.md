### Ricorsione
<- [RETURN](https://github.com/niksolaz/Algorithm-doc/tree/develop?tab=readme-ov-file)

#### Descrizione Breve
La ricorsione è una tecnica di programmazione in cui una funzione chiama sé stessa per risolvere un problema più grande, suddividendolo in sottoproblemi più piccoli e più gestibili. È particolarmente utile per problemi che possono essere suddivisi in sottoproblemi simili a sé stessi.

#### Codice di Esempio in Python

**Fattoriale di un numero (n!):**
```python
def factorial(n):
    if n == 0 or n == 1:
        return 1
    else:
        return n * factorial(n - 1)

# Esempio di utilizzo
print(factorial(5))  # Output: 120
```

**Fibonacci:**
```python
def fibonacci(n):
    if n <= 0:
        return 0
    elif n == 1:
        return 1
    else:
        return fibonacci(n - 1) + fibonacci(n - 2)

# Esempio di utilizzo
print(fibonacci(6))  # Output: 8
```

#### Pro e Contro

**Pro:**
1. **Eleganza e semplicità:** Il codice ricorsivo può essere più semplice e più vicino alla descrizione del problema.
2. **Facilità di suddivisione del problema:** Alcuni problemi sono naturalmente ricorsivi, rendendo la soluzione ricorsiva intuitiva.
3. **Meno codice:** Spesso richiede meno righe di codice rispetto alla soluzione iterativa.

**Contro:**
1. **Overhead di stack:** Ogni chiamata ricorsiva aggiunge un nuovo frame allo stack, il che può portare a un "stack overflow" per problemi di grandi dimensioni.
2. **Prestazioni:** La ricorsione può essere meno efficiente dell'iterazione a causa dell'overhead delle chiamate di funzione.
3. **Difficoltà di debugging:** Il debugging di codice ricorsivo può essere più complesso rispetto al codice iterativo.

#### Casi d'Uso

- **Problemi naturalmente ricorsivi:**
  - Alberi (traversal di alberi binari)
  - Problemi di divisione e conquista (quicksort, mergesort)
  - Problemi di ricerca (backtracking, risoluzione di labirinti)
  
- **Algoritmi matematici:**
  - Calcolo del fattoriale
  - Serie di Fibonacci

- **Algoritmi grafici:**
  - Algoritmi di riempimento (flood fill)

La ricorsione è una tecnica potente e elegante per risolvere problemi, ma deve essere usata con attenzione per evitare problemi di prestazioni e stack overflow.
<- [RETURN](https://github.com/niksolaz/Algorithm-doc/tree/develop?tab=readme-ov-file)