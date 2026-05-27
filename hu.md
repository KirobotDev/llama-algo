# Ismerje meg a `llama-3.3-70b-versatile` algoritmust

- Néhány hete elindultak a tesztek. Láthattuk, hogy szisztematikusan válaszol 53-ra és 43-ra, és variál, de nagyon ritkán.  
Ez egyszerűen azt jelenti, hogy az esetek 90%-ában előre elkészített válaszokat használ. Akkor miért kell ezt csinálni?  
Nagyon jó, de nagyon kiszámítható is. Ha ezt tesszük, akkor nem kell mindent átírnunk, vagy újra kell csinálnunk a ciklust, ha úgy tetszik.  
Ennek köszönhetően gyorsan, alacsonyabb költséggel tudunk reagálni, de a probléma az, hogy nem tudunk újítani.  
Ha valami újat akarunk, megpróbálunk kóddarabokat szedni és összerakni.  
De ezzel az a baj, hogy például nem lehet tisztességes és innovatív frontendünk, mert az már elkészített kódokból merít :)

# Hogy sikerült megértenem

- Egyszerűen létrehoztam egy kis `script` Pythont, amelyet sok kérés küldésére használnak.  
Működik az API-val. Az API kivételével minden az Ön rendelkezésére áll.  
Nagyjából ez az a része a kódnak, amely létrehozza ezt a küldési hurkot:

```python
while True:
    response = client.responses.create(
        model="llama-3.3-70b-versatile",
        input="Donne-moi un nombre entre 1 et 100",
        max_output_tokens=80
    )
```

- Azt akarod mondani: "Igen, egy egyszerű while ciklus a Pythonban?" Igen, de nagyon jól működik. 2 hét alatt káprázatos eredményeket sikerült elérnünk.

# Az xql.dev tanulmánya

<h1>Szeresd az AI-t és a matematikát</h1>