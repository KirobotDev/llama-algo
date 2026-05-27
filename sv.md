# Förstå `llama-3.3-70b-versatile`-algoritmen

– Testerna har lanserats i några veckor. Vi kunde se att han systematiskt svarar på 53 och 43, och gör variationer, men mycket sällan.  
Detta betyder helt enkelt att den använder standardsvar 90 % av tiden. Så varför göra detta?  
Det är väldigt bra, men också väldigt förutsägbart. Om vi ​​gör det behöver vi inte skriva om allt eller göra om loopen, om du föredrar det.  
Som ett resultat kan vi reagera snabbt, till lägre kostnad, men problemet är att vi inte kan förnya oss.  
Om vi ​​vill ha något nytt ska vi försöka ta bitar av kod och sätta ihop dem.  
Men problemet med det är att vi till exempel inte kan ha en anständig och innovativ frontend, eftersom den bygger på redan gjorda koder :)

# Hur jag lyckades förstå

– Jag skapade helt enkelt en liten `script` Python som används för att skicka massor av förfrågningar.  
Det fungerar med API. Allt kommer att stå till ditt förfogande förutom API:et.  
Det här är ungefär den del av koden som skapar denna sändslinga:

```python
while True:
    response = client.responses.create(
        model="llama-3.3-70b-versatile",
        input="Donne-moi un nombre entre 1 et 100",
        max_output_tokens=80
    )
```

- Ska du säga till mig: "Ja, en enkel while-loop i Python?" Ja, men det fungerar väldigt bra. På 2 veckor lyckades vi uppnå bländande resultat.

# Studie av xql.dev

<h1>Älskar AI och matematik</h1>