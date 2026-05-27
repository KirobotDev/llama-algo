# Forstå `llama-3.3-70b-versatile`-algoritmen

– Testene har vært lansert i noen uker. Vi kunne se at han systematisk svarer på 53 og 43, og gjør variasjoner, men svært sjelden.  
Dette betyr ganske enkelt at den bruker hermetiske svar 90 % av tiden. Så hvorfor gjøre dette?  
Det er veldig bra, men også veldig forutsigbart. Hvis vi gjør det, trenger vi ikke å skrive om alt eller gjøre om loopen, hvis du foretrekker det.  
Som et resultat kan vi reagere raskt, til lavere kostnad, men problemet er at vi ikke kan innovere.  
Hvis vi vil ha noe nytt, prøver vi å ta kodebiter og sette dem sammen.  
Men problemet med det er at vi for eksempel ikke kan ha en grei og innovativ frontend, fordi den trekker på koder som allerede er laget :)

# Hvordan jeg klarte å forstå

– Jeg har rett og slett laget en liten `script` Python som brukes til å sende mange forespørsler.  
Det fungerer med API. Alt vil være til din disposisjon bortsett fra API.  
Dette er omtrent den delen av koden som lager denne sendeløkken:

```python
while True:
    response = client.responses.create(
        model="llama-3.3-70b-versatile",
        input="Donne-moi un nombre entre 1 et 100",
        max_output_tokens=80
    )
```

- Skal du si til meg: "Ja, en enkel while-løkke i Python?" Ja, men det fungerer veldig bra. På 2 uker klarte vi å oppnå blendende resultater.

# Studie av xql.dev

<h1>Elsker AI og matematikk</h1>