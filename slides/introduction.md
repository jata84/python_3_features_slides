# Python Features 3.5 > 
### Novedades del lenguaje desde la versión 3.5 a la 3.8

						<div style="width: 100% ;overflow: hidden;">
						<div style="float: left; width:50%" class="fragment">
														<p>Sin Soporte de Tipado</p>
								<pre><code style="font-size: 15px;line-height : 15px;" data-trim data-noescape>
def factorial(i: int) -> int:
	if i<0:
		return None 
	if i==0:
		return 1
	return i*factorial(i-1)
print(factorial(3.3))

Traceback (most recent call last):
 .....
TypeError: unsupported operand type(s) for *: 
'float' and 'NoneType'
								</code></pre>
						</div>
						<div style="float: left; width:50%" class="fragment">
							<p>Con soporte de tipado</p>
								<pre><code style="font-size: 15px;line-height : 15px;" data-trim data-noescape>
def factorial(i: int) -> int:
	if i<0:
		return None
	if i==0:
		return 1
	return i*factorial(i-1)
print(factorial(3.3))
 .....
python35_typehint.py:3: error: 
Incompatible return value type (got "None", expected "int")
python35_typehint.py:9: error: 
Argument 1 to "factorial" has incompatible type "float"; expected "int"
Found 2 errors in 1 file (checked 1 source file)

								</code></pre>
						</div>
						</div>