### Selection Sort

#### Descrizione Breve
Selection Sort è un algoritmo di ordinamento semplice che divide l'array in due parti: una parte ordinata e una parte non ordinata. Il processo ripetutamente seleziona il minimo (o massimo) elemento dalla parte non ordinata e lo sposta alla fine della parte ordinata.

#### Codice di Esempio in Python
```python
def selection_sort(arr):
    n = len(arr)
    for i in range(n):
        min_index = i
        for j in range(i+1, n):
            if arr[j] < arr[min_index]:
                min_index = j
        arr[i], arr[min_index] = arr[min_index], arr[i]
    return arr

# Esempio di utilizzo
array = [64, 25, 12, 22, 11]
sorted_array = selection_sort(array)
print(sorted_array)  # Output: [11, 12, 22, 25, 64]
```

#### Pro e Contro

**Pro:**
1. **Semplicità:** Facile da comprendere e implementare.
2. **Stabile rispetto alla memoria:** Funziona in-place, non necessita di memoria aggiuntiva significativa.
3. **Deterministico:** Sempre termina con un array ordinato.

**Contro:**
1. **Inefficiente per grandi dataset:** Ha una complessità temporale di O(n^2), il che lo rende impraticabile per dataset di grandi dimensioni.
2. **Non stabile:** Non preserva l'ordine relativo degli elementi con valori uguali (a meno che non venga implementato un accorgimento specifico).

#### Casi d'Uso
- **Dataset piccoli:** Può essere utile per ordinare piccoli array o dataset dove la semplicità del codice è più importante delle prestazioni.
- **Contesti educativi:** Ottimo per spiegare i concetti base degli algoritmi di ordinamento e la loro implementazione.
- **Situazioni con limitate risorse di memoria:** Poiché non richiede spazio extra, è utile quando la memoria è una risorsa critica.

Selection Sort è una buona scelta per casi semplici e didattici, ma non è adatto per l'uso pratico su dataset di grandi dimensioni a causa della sua inefficienza.