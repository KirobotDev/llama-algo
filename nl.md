# Begrijp het `llama-3.3-70b-versatile`-algoritme

- De tests zijn sinds een paar weken gelanceerd. We konden zien dat hij systematisch de vragen 53 en 43 beantwoordt, en daar variaties op maakt, maar zeer zelden.  
Dit betekent simpelweg dat het 90% van de tijd standaardantwoorden gebruikt. Dus waarom dit doen?  
Het is erg goed, maar ook erg voorspelbaar. Als we dat doen, hoeven we niet alles te herschrijven of de lus opnieuw uit te voeren, als je dat liever hebt.  
Hierdoor kunnen we snel reageren, tegen lagere kosten, maar het probleem is dat we niet kunnen innoveren.  
Als we iets nieuws willen, proberen we stukjes code te nemen en deze samen te voegen.  
Maar het probleem daarmee is dat we bijvoorbeeld geen fatsoenlijke en innovatieve frontend kunnen hebben, omdat deze gebruik maakt van reeds gemaakte codes :)

# Hoe ik het wist te begrijpen

- Ik heb eenvoudigweg een kleine `script` Python gemaakt die wordt gebruikt om veel verzoeken te verzenden.  
Het werkt met de API. Alles staat tot uw beschikking behalve de API.  
Dit is grofweg het deel van de code dat deze verzendlus creëert:

```python
while True:
    response = client.responses.create(
        model="llama-3.3-70b-versatile",
        input="Donne-moi un nombre entre 1 et 100",
        max_output_tokens=80
    )
```

- Ga je me vertellen: "Ja, een simpele while-lus in Python?" Ja, maar het werkt heel goed. Binnen 2 weken hebben we verbluffende resultaten weten te bereiken.

# Onderzoek door xql.dev

<h1>Ik hou van AI en wiskunde</h1>