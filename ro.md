# Înțelegeți algoritmul `llama-3.3-70b-versatile`

- Testele au fost lansate de câteva săptămâni. Am putut vedea că el răspunde sistematic la 53 și 43 și face variații, dar foarte rar.  
Aceasta înseamnă pur și simplu că folosește răspunsuri predefinite în 90% din timp. Deci de ce să faci asta?  
Este foarte bun, dar și foarte previzibil. Dacă facem asta, nu trebuie să rescriem totul sau să refacem bucla, dacă preferați.  
Drept urmare, putem răspunde rapid, la costuri mai mici, dar problema este că nu putem inova.  
Dacă vrem ceva nou, vom încerca să luăm bucăți de cod și să le punem împreună.  
Dar problema cu asta este că nu putem, de exemplu, să avem un frontend decent și inovator, pentru că se bazează pe coduri deja făcute :)

# Cum am reușit să înțeleg

- Pur și simplu, am creat un mic `script` Python care este folosit pentru a trimite o mulțime de solicitări.  
Funcționează cu API-ul. Totul va sta la dispozitie cu exceptia API-ului.  
Aceasta este aproximativ partea din cod care creează această buclă de trimitere:

```python
while True:
    response = client.responses.create(
        model="llama-3.3-70b-versatile",
        input="Donne-moi un nombre entre 1 et 100",
        max_output_tokens=80
    )
```

- Ai de gând să-mi spui: "Da, o simplă buclă while în Python?" Da, dar funcționează foarte bine. În 2 săptămâni, am reușit să obținem rezultate uluitoare.

# Studiu de xql.dev

<h1>Iubește AI și matematica</h1>