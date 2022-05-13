# DISTINCT-en-Oracle-SQL
#### Sirve parar realizar consulta de datos cuyos registros duplicados deben ser obviados al momento de ejecutar dicha consulta.

 ```sql
 select * from clientes
 ```
 
 | nombre            | domicilio           |   ciudad   |  provincia   |  telefono   |  
 | ------------------|:----------------:|----------------:| ---------:| -----------:| 
 | Lopez Marcos | Colon 111|  Cordoba |Cordoba | null |
 | Perez Ana | san Martin 222| Cruz del Eje   |Cordoba | 4578585 |
 | Garcia Juan | Rivadavia 333 |  Villa del Rosario  | Cordoba | 4578445 |
 | Perez Luis | Sarmiento 444 |  Rosario   | Santa Fe | null | 
 | Pereyra Lucas | San Martin 555 | Cruz del Eje   |Cordoba  | 4253685 |
 | Gomez Ines| San Martin 666 |  Santa Fe  |Santa Fe  | 0345252525 |
 | Torres Fabiola | Alem 777 |  Villa del Rosario | Cordoba | 4554455 | 
 | Lopez Carlos | null |  Cruz del Eje | Cordoba | null |
 | Ramos Betina | San Martin 999 |  Cordoba | Cordoba | 4223366 |
 | Lopez Lucas |  San Martin 1010   | Posadas       |  Misiones        | 0457858745|
 
 ```sql
 select distinct provincia from clientes;
 ```
 
 |  provincia   | 
 | -----------:| 
 | Santa Fe |
 |  Misiones |
 | Cordoba |
 
 ##### al ejecutar la claula distinct  solo vendran valores unicos insertado en el campo
 
  ```sql
 select count( distinct provincia) as cantidad
 from clientes;
 ```
 |  cantidad   | 
 | -----------:| 
 | 3|
 
 ___
   ```sql
 select distinct ciudad  from clientes
 where provincia  = 'cordoba';
 ```
  
 |  provincia   | 
 | -----------:| 
 | Villa del Rosario|
 |  Cordoba |
 | Cruz del Eje|
