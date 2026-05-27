# Forstå `llama-3.3-70b-versatile`-algoritmen

- Testene har været sat i gang i nogle uger. Vi kunne se, at han systematisk besvarer 53 og 43, og laver variationer, men meget sjældent.  
Dette betyder simpelthen, at den bruger konserverede svar 90 % af tiden. Så hvorfor gøre dette?  
Det er meget godt, men også meget forudsigeligt. Hvis vi gør det, behøver vi ikke at omskrive alt eller lave loopet om, hvis du foretrækker det.  
Som et resultat kan vi reagere hurtigt til lavere omkostninger, men problemet er, at vi ikke kan innovere.  
Hvis vi vil have noget nyt, vil vi prøve at tage stykker kode og sætte dem sammen.  
Men problemet med det er, at vi for eksempel ikke kan have en anstændig og innovativ frontend, fordi den trækker på allerede lavet koder :)

# Hvordan jeg formåede at forstå

- Jeg lavede simpelthen en lille `script` Python, som bruges til at sende en masse forespørgsler.  
Det virker med API'et. Alt vil være til din rådighed undtagen API.  
Dette er nogenlunde den del af koden, der skaber denne sendeløkke:

```python
while True:
    response = client.responses.create(
        model="llama-3.3-70b-versatile",
        input="Donne-moi un nombre entre 1 et 100",
        max_output_tokens=80
    )
```

- Vil du sige til mig: "Ja, en simpel while-løkke i Python?" Ja, men det fungerer meget godt. På 2 uger lykkedes det os at opnå blændende resultater.

# Undersøgelse af xql.dev

<h1>Elsker AI og matematik</h1>