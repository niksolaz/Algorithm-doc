### QuickSort
<- [RETURN](https://github.com/niksolaz/Algorithm-doc/tree/develop?tab=readme-ov-file)

#### Descrizione Breve
QuickSort è un algoritmo di ordinamento efficiente basato sulla strategia "divide et impera". Seleziona un "pivot" e partiziona l'array in due sottosequenze: una contenente elementi minori del pivot e l'altra contenente elementi maggiori. Successivamente, ordina ricorsivamente le sottosequenze.

#### Codice di Esempio in Python
```python
def quicksort(arr):
    if len(arr) <= 1:
        return arr
    else:
        pivot = arr[len(arr) // 2]
        left = [x for x in arr if x < pivot]
        middle = [x for x in arr if x == pivot]
        right = [x for x in arr if x > pivot]
        return quicksort(left) + middle + quicksort(right)

# Esempio di utilizzo
array = [3, 6, 8, 10, 1, 2, 1]
sorted_array = quicksort(array)
print(sorted_array)  # Output: [1, 1, 2, 3, 6, 8, 10]
```

#### Pro e Contro

**Pro:**
1. **Efficiente nella pratica:** Ha una complessità media di O(n log n) e una buona efficienza sui dati reali.
2. **In-place e non in-place:** Può essere implementato sia in-place, risparmiando memoria, sia non in-place, come nell'esempio sopra, per maggiore chiarezza.
3. **Divide et impera:** Facile da implementare in modo parallelo.

**Contro:**
1. **Caso peggiore:** La complessità nel caso peggiore è O(n^2), anche se può essere mitigata con una buona scelta del pivot (ad esempio, usando il "median of three").
2. **Non stabile:** Non preserva l'ordine relativo degli elementi uguali, a meno che non venga implementato in modo specifico per essere stabile.
3. **Overhead della ricorsione:** La ricorsione può portare a un consumo significativo di stack, specialmente su input di grandi dimensioni.

#### Casi d'Uso

- **Ordinamento generale:** È ampiamente utilizzato per ordinare array e liste di dati in applicazioni reali.
- **Librerie standard:** Molte librerie di linguaggi di programmazione utilizzano QuickSort o una sua variante (ad esempio, "Introsort" che combina QuickSort e HeapSort) come algoritmo di ordinamento predefinito.
- **Applicazioni parallele:** Grazie alla sua natura "divide et impera", può essere facilmente parallelizzato per migliorare le prestazioni su macchine multi-core.
- **Sistemi embedded:** Può essere utilizzato in contesti dove la memoria è una risorsa critica, grazie alla sua versione in-place.

QuickSort è un algoritmo potente e versatile, adatto a molte applicazioni pratiche di ordinamento, sebbene richieda attenzione nella scelta del pivot per garantire prestazioni ottimali.
<- [RETURN](https://github.com/niksolaz/Algorithm-doc/tree/develop?tab=readme-ov-file)