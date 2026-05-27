# Comprender el algoritmo `llama-3.3-70b-versatile`

- Las pruebas se han iniciado desde hace algunas semanas. Pudimos ver que responde sistemáticamente a 53 y 43, y hace variaciones, pero muy raramente.  
Esto simplemente significa que utiliza respuestas predeterminadas el 90% del tiempo. Entonces, ¿por qué hacer esto?  
Es muy bueno, pero también muy predecible. Si hacemos eso, no necesitamos reescribir todo ni rehacer el ciclo, si lo prefiere.  
Como resultado, podemos responder rápidamente y a menor costo, pero el problema es que no podemos innovar.  
Si queremos algo nuevo, intentaremos tomar fragmentos de código y juntarlos.  
Pero el problema con esto es que no podemos, por ejemplo, tener una interfaz decente e innovadora, porque se basa en códigos ya creados :)

# Cómo logré entender

- Simplemente, creé un pequeño `script` Python que se usa para enviar muchas solicitudes.  
Funciona con la API. Todo estará a tu disposición excepto la API.  
Esta es aproximadamente la parte del código que crea este bucle de envío:

```python
while True:
    response = client.responses.create(
        model="llama-3.3-70b-versatile",
        input="Donne-moi un nombre entre 1 et 100",
        max_output_tokens=80
    )
```

- ¿Me vas a decir: "Sí, un bucle while simple en Python?" Sí, pero funciona muy bien. En 2 semanas, logramos lograr resultados deslumbrantes.

# Estudio realizado por xql.dev

<h1>Me encanta la IA y las matemáticas</h1>