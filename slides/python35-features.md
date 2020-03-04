#### Python 3.5 
- Su última versión sale en 2015
- Estará soportado hasta 2020



#### PEP 492
- corutines con sintaxis async y await
- Incorporación de palabras clave para async y await que facilitan el trabajo con asyncio
- Ya no es necesario usar los decoradores


#### Sintaxis async y await

Declaración de corutinas con async
```python 
	async def read_data(db):
		pass
```
Expresión await para capturar el resultado de una corutina

```python 
	async def read_data(db):
	    data = await db.fetch('SELECT ...')
```

Gestores de contexto asincronos:
```python 
	async def commit(session, data):
	    async with session.transaction():
	        await session.update(data)
```


#### PEP 484 Type Hints
- Soporte en tiempo de ejecución para el tipado
- Funciones de ayuda para crear distintos tipos
- Tipo Any

Soporte en tiempo de ejecución:
```python 
	def greeting(name: str) -> str:
	    return 'Hello ' + name
```
Funciones de ayuda para crear distintos tipos
```python 
	from typing import NewType

	UserId = NewType('UserId', int)
	some_id = UserId(524313)
```