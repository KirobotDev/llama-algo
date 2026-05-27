# Verstehen Sie den `llama-3.3-70b-versatile`-Algorithmus

- Die Tests laufen seit einigen Wochen. Wir konnten sehen, dass er die Fragen 53 und 43 systematisch beantwortet und Variationen vornimmt, aber sehr selten.  
Das bedeutet einfach, dass in 90 % der Fälle vorgefertigte Antworten verwendet werden. Warum also das tun?  
Es ist sehr gut, aber auch sehr vorhersehbar. Wenn wir das tun, müssen wir nicht alles neu schreiben oder die Schleife wiederholen, wenn Sie möchten.  
Dadurch können wir schnell und zu geringeren Kosten reagieren, das Problem besteht jedoch darin, dass wir keine Innovationen einführen können.  
Wenn wir etwas Neues wollen, versuchen wir, Teile des Codes zu nehmen und sie zusammenzusetzen.  
Das Problem dabei ist jedoch, dass wir beispielsweise kein anständiges und innovatives Frontend haben können, weil es auf bereits erstellten Codes basiert :)

# Wie ich es geschafft habe zu verstehen

- Ich habe einfach ein kleines `script`-Python erstellt, das zum Senden vieler Anfragen verwendet wird.  
Es funktioniert mit der API. Bis auf die API steht Ihnen alles zur Verfügung.  
Dies ist ungefähr der Teil des Codes, der diese Sendeschleife erstellt:

```python
while True:
    response = client.responses.create(
        model="llama-3.3-70b-versatile",
        input="Donne-moi un nombre entre 1 et 100",
        max_output_tokens=80
    )
```

- Wirst du mir sagen: „Ja, eine einfache While-Schleife in Python?“ Ja, aber es funktioniert sehr gut. Innerhalb von 2 Wochen konnten wir umwerfende Ergebnisse erzielen.

# Studie von xql.dev

<h1>Ich liebe KI und Mathematik</h1>