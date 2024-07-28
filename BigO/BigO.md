<- [RETURN](https://github.com/niksolaz/Algorithm-doc/tree/develop?tab=readme-ov-file)

Il calcolo del Big O è un modo per descrivere l'efficienza di un algoritmo in termini di tempo o spazio in funzione della dimensione dell'input. La notazione Big O rappresenta il comportamento asintotico di un algoritmo, ossia come si comporta quando la dimensione dell'input tende all'infinito. Di seguito spiego come si calcola e si interpreta il Big O per diversi tipi di complessità.

### O(1) - Tempo Costante
Un algoritmo ha complessità O(1) se il tempo di esecuzione è indipendente dalla dimensione dell'input. Ad esempio, accedere a un elemento di un array per indice è O(1).

**Esempio:**
```python
def access_element(array, index):
    return array[index]
```

### O(n) - Tempo Lineare
Un algoritmo ha complessità O(n) se il tempo di esecuzione cresce linearmente con la dimensione dell'input. Scorrere tutti gli elementi di un array è un esempio classico.

**Esempio:**
```python
def print_elements(array):
    for element in array:
        print(element)
```

### O(log n) - Tempo Logaritmico
Un algoritmo ha complessità O(log n) se il tempo di esecuzione cresce logaritmicamente con la dimensione dell'input. Gli algoritmi di ricerca binaria sono un esempio tipico.

**Esempio:**
```python
def binary_search(array, target):
    left, right = 0, len(array) - 1
    while left <= right:
        mid = (left + right) // 2
        if array[mid] == target:
            return mid
        elif array[mid] < target:
            left = mid + 1
        else:
            right = mid - 1
    return -1
```

### O(n^2) - Tempo Quadratico
Un algoritmo ha complessità O(n^2) se il tempo di esecuzione cresce proporzionalmente al quadrato della dimensione dell'input. Gli algoritmi di ordinamento come Bubble Sort sono esempi comuni.

**Esempio:**
```python
def bubble_sort(array):
    n = len(array)
    for i in range(n):
        for j in range(0, n-i-1):
            if array[j] > array[j+1]:
                array[j], array[j+1] = array[j+1], array[j]
```

### O(n log n) - Tempo Quasi Lineare
Un algoritmo ha complessità O(n log n) se il tempo di esecuzione cresce in modo proporzionale alla dimensione dell'input moltiplicato per il logaritmo della dimensione dell'input. Gli algoritmi di ordinamento efficienti come Merge Sort e Quick Sort hanno questa complessità.

**Esempio:**
```python
def merge_sort(array):
    if len(array) > 1:
        mid = len(array) // 2
        left_half = array[:mid]
        right_half = array[mid:]

        merge_sort(left_half)
        merge_sort(right_half)

        i = j = k = 0

        while i < len(left_half) and j < len(right_half):
            if left_half[i] < right_half[j]:
                array[k] = left_half[i]
                i += 1
            else:
                array[k] = right_half[j]
                j += 1
            k += 1

        while i < len(left_half):
            array[k] = left_half[i]
            i += 1
            k += 1

        while j < len(right_half):
            array[k] = right_half[j]
            j += 1
            k += 1
```

### Come Calcolare il Big O
1. **Identifica le operazioni dominanti:** Concentrati sulle operazioni che si ripetono più frequentemente e che hanno il maggiore impatto sul tempo di esecuzione.
2. **Elimina le costanti:** Le costanti non influenzano la complessità asintotica, quindi si ignorano.
3. **Considera il caso peggiore:** Il Big O descrive il comportamento nel caso peggiore, per garantire un limite superiore sulla complessità dell'algoritmo.
4. **Utilizza le proprietà matematiche:** Quando sommi termini, prendi il termine con la maggiore crescita (e.g., O(n + n^2) = O(n^2)). Quando moltiplichi, mantieni entrambi i termini (e.g., O(n * log n)).

### Esempio Pratico
Consideriamo un algoritmo che scorre un array e poi esegue una ricerca binaria su un altro array. La complessità sarà la somma delle complessità dei due passaggi principali.

**Esempio:**
```python
def example_algorithm(array1, array2, target):
    for element in array1:  # Questo è O(n)
        print(element)
    return binary_search(array2, target)  # Questo è O(log n)
```
La complessità totale sarà O(n) per il ciclo e O(log n) per la ricerca binaria. Poiché O(n) domina O(log n), la complessità complessiva è O(n).

Con queste basi, dovresti essere in grado di analizzare la complessità di vari algoritmi e comprendere come ottimizzarli per migliorare l'efficienza. Se hai altri esempi specifici o domande su algoritmi particolari, non esitare a chiedere.

<- [RETURN](https://github.com/niksolaz/Algorithm-doc/tree/develop?tab=readme-ov-file)