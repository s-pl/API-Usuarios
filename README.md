
# API de Gestión de Usuarios

La API proporciona un conjunto de servicios para la gestión de usuarios en un sistema. Permite realizar operaciones como añadir usuarios, eliminar usuarios, consultar información de usuarios y actualizar datos de usuarios.

El directorio ```public``` no es necesario para el funcionamiento de la API y es solo una simple demostración de cómo funciona, en ningun caso estos archivos deberian ser usados en el producto final.




## Uso de la API

#### Añadir un usuario
```http
  POST /usuarios/a-usuario
```

| Parametro | Tipo     | Descripcion              |
| :-------- | :------- | :------------------------- |
| `nombre` | `string` | **Requerido**.|
| `apellidos` | `string` | **Requerido**.||
| `dni` | `string` | **Requerido**.|
| `foto` | `string` | **Requerido**.|
| `fechaValidez` | `string` | **Requerido**.|
| `key` | `string` | **Requerido**.|



#### Eliminar usuario

```http
  POST /usuarios/eliminar-usuario
```

| Parametro | Tipo     | Descripcion                       |
| :-------- | :------- | :-------------------------------- |
| `id`      | `string` | **Requerido**.  DNI del usuario|
| `key`      | `string` | **Requerido**.  Tu clave secreta|

#### Consulta al servidor por un usuario en específico

```http
  POST /usuarios/consultar-usuario
```

| Parametro | Tipo     | Descripcion                      |
| :-------- | :------- | :-------------------------------- |
| `id`      | `string` | **Requerido**.  DNI del usuario|
| `key`      | `string` | **Requerido**.  Tu clave secreta|

#### Renovar a un usuario especificando una nueva fecha de válidez

```http
  POST /usuarios/actualizar-usuario
```

| Parametro | Tipo     | Descripcion                       |
| :-------- | :------- | :-------------------------------- |
| `id`      | `string` | **Requerido**.  DNI del usuario|
| `key`      | `string` | **Requerido**.  Tu clave secreta|
| `NuevaFecha`      | `string` | **Requerido**.  La fecha de renovación|



## Inicialización

Para inicializar el proyecto cambia el valor ```KEY``` en el ```.env```

``` .env
  KEY=(Tu clave)
```

¡Cualquiera que tenga acceso a esta key tendrá acceso a la base de datos del servidor!
    
## Licencia

[MIT](https://choosealicense.com/licenses/mit/)

```MIT License

Copyright (c) 2024 Samuel Ponce Luna

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.```


