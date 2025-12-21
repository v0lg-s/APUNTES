Permiten maniuplar los bits de datos individuales. Cubren las operaciones del contexto lógico (**AND, OR, NOT**) y un operador adicional **XOR**. Todos a nivel de bits y no de verdad o lógica.

- `&`: AND a nivel de bits (Conjunción)
- `|`: OR  a nivel de bits (Disyunción)
- `~`: NOT a nivel de bits (Negación)
- `^`: XOR a nivel de bits.

*Ejemplo propio de utilidad:*
Cuando necesitamos conocer la dirección de red de una dirección de host dada. (Ver: [[Hallar dirección de subred de una dirección IP dada]]).

tenemos un host con la dirección IP **172.33.43.5** con máscara **255.255.224.0 = /19**, para conocer la dirección de red tenemos que hacer la operación AND entre la IP dada y su máscara de red.

![[Hallar dirección de subred de una dirección IP dada#^6c546e]]

![[Hallar dirección de subred de una dirección IP dada#^5bf495]]

En python:

```python
host_ip = [172,33,43,5]
mask = [255,255,224,0]

net = [i & m for i, m in zip(host_ip, mask)]

# salida de zip(ip, mask): [(172,255), (33,255), (43,224), (5,0)]
# net = [172,33,32,0]
```

# Propiedades
- **Conmutativa:** El orden de los operandos no importa.
    - `A & B` es igual a `B & A`.
    - `A | B` es igual a `B | A`.
    - `A ^ B` es igual a `B ^ A`.
- **Asociativa:** Para operaciones con múltiples operandos del mismo tipo.
    - `(A & B) & C` es igual a `A & (B & C)`.
- **Idempotencia:** Aplicar la operación consigo misma devuelve el mismo valor.
    - `A & A = A`
    - `A | A = A`
- **Propiedad de identidad (elementos neutros):**
    - `A & 1 = A` (el bit 1 es la identidad para AND).
    - `A | 0 = A` (el bit 0 es la identidad para OR).
- **Propiedades de Absorción:**
    - `A & (A | B) = A`.
    - `A | (A & B) = A`.
- **Inversión (XOR):**
    - `A ^ A = 0`.
    - `A ^ 0 = A`.
    - `A ^ 1` invierte todos los bits de `A`.