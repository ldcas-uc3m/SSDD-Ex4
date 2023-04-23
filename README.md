# Ejercicio Evaluable 4: Diseño de una aplicación distribuida
By Luis Daniel Casais Mezquida & Lucía María Moya Sans  
Sistemas Distribuídos 22/23  
Bachelor's Degree in Computer Science and Engineering, grp. 89  
Universidad Carlos III de Madrid

## Descripción del ejercicio
Considere un supermercado con 10 cajas donde los clientes pueden realizar sus pagos. Se desea desarrollar un sistema que permita conocer el estado de cada caja. Cada caja registra las ventas totales que se han realizado desde que se abrió. El funcionamiento de cada caja es el siguiente:
1. Cuando el cajero abre la caja, el computador que la controla envía un mensaje a un computador central que registra la actividad de todas las cajas del supermercado. El mensaje debe incluir, entre otros, el identificador del cajero que abre la caja, el número de caja y la hora de apertura.
2. Cada vez que se realiza una venta en una caja, el computador que la controla envía un mensaje al computador central indicando, entre otros, el identificador del cajero, el número de caja, hora de venta e importe total. Además, debe enviar la lista de todos los artículos que se han vendido en ese momento. Esta lista debe incluir, al menos, el identificador del producto y el importe del mismo.
3. Cuando el cajero cierra la caja, el computador que la controla envía un mensaje al computador central que registra la actividad de todas las cajas del supermercado. En este caso se envía la cantidad total de artículos que se han facturado desde la última apertura, el número de minutos que ha estado abierta y la cantidad total de dinero que se ha facturado.
4. En cualquier momento, un usuario desde el computador central puede monitorizar el estado de cada caja. En este caso, la caja responde indicando si está abierta o cerrada. En caso de estar abierta devuelve el identificador del cajero que abrió la caja, el número de minutos que lleva abierta, el número total de artículos facturados y la cantidad total facturada hasta ese momento.

Se quiere diseñar una aplicación distribuida que se encargue de gestionar el sistema anteriormente
descrito utilizando sockets.