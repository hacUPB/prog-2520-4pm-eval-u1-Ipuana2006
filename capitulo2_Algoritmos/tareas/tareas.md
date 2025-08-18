# TAREAS 
1. Realice el algoritmo para determinar cuánto pagará una persona que adquiera N artículos, los cuales están de promoción. Considere que si su precio es mayor o igual a $200 se le aplica un descuento de 15%, y si su precio es mayor a $100 pero menor a $200, el descuento es de 12%; De lo contrario, sólo se le aplica 10%. Se debe saber cuál es el costo y el descuento que tendrá cada uno de los artículos y finalmente te cuánto se pagará por todos los artículos obtenidos. Representa la solución mediante el diagrama de flujo, el pseudocódigo y el diagrama N/S.
## Solucion 

## Pseudocódigo
```
INICIO
  LEER N   // número de artículos
  TOTAL = 0

  PARA i = 1 HASTA N HACER
     LEER PRECIO
     SI PRECIO >= 200 ENTONCES
         DESCUENTO = PRECIO * 0.15
     SINO
         SI PRECIO > 100 ENTONCES
             DESCUENTO = PRECIO * 0.12
         SINO
             DESCUENTO = PRECIO * 0.10
         FIN SI
     FIN SI

     PRECIO_FINAL = PRECIO - DESCUENTO
     ESCRIBIR "Artículo ", i, ": Costo=", PRECIO, 
              " Descuento=", DESCUENTO, 
              " Precio final=", PRECIO_FINAL

     TOTAL = TOTAL + PRECIO_FINAL
  FIN PARA

  ESCRIBIR "TOTAL A PAGAR = ", TOTAL
FIN
 ```
 2. Tienen una tarjeta de $10.000.000. Calcular el valor de todas las cuotas sabiendo:

- Valor de la compra
- Tasa de interés del 2%
- Número de cuotas. Máximo 36.

## Solución 

## Pseudocódigo
```
INICIO
  LEER TOTAL        // valor de la compra
  LEER N_CUOTAS     // número de cuotas, máximo 36
  i = 0.02          // tasa de interés mensual

  SI N_CUOTAS > 36 ENTONCES
     ESCRIBIR "No puede superar 36 cuotas"
  SINO
     CUOTA = (TOTAL * i) / (1 - (1 + i)^(-N_CUOTAS))
     ESCRIBIR "Valor de cada cuota = ", CUOTA
     ESCRIBIR "Total pagado = ", CUOTA * N_CUOTAS
     ESCRIBIR "Intereses = ", (CUOTA * N_CUOTAS) - TOTAL
  FIN SI
FIN
```