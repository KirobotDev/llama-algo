# Ymmärrä `llama-3.3-70b-versatile`-algoritmi

– Testit on käynnistetty muutaman viikon ajan. Voisimme nähdä, että hän vastaa systemaattisesti 53 ja 43 ja tekee muunnelmia, mutta hyvin harvoin.  
Tämä tarkoittaa yksinkertaisesti sitä, että se käyttää valmiita vastauksia 90 % ajasta. Joten miksi tehdä tämä?  
Se on erittäin hyvä, mutta myös hyvin ennakoitavissa. Jos teemme niin, meidän ei tarvitse kirjoittaa kaikkea uudelleen tai tehdä silmukkaa uudelleen, jos haluat.  
Tämän seurauksena voimme reagoida nopeasti ja pienemmillä kustannuksilla, mutta ongelmana on, että emme voi innovoida.  
Jos haluamme jotain uutta, yritämme ottaa koodinpätkiä ja koota ne yhteen.  
Mutta ongelma tässä on se, että meillä ei esimerkiksi voi olla kunnollista ja innovatiivista käyttöliittymää, koska se hyödyntää jo tehtyjä koodeja :)

# Kuinka onnistuin ymmärtämään

- Yksinkertaisesti loin pienen `script` Pythonin, jota käytetään lähettämään paljon pyyntöjä.  
Se toimii API:n kanssa. Kaikki on käytettävissäsi paitsi API.  
Tämä on suunnilleen se osa koodia, joka luo tämän lähetyssilmukan:

```python
while True:
    response = client.responses.create(
        model="llama-3.3-70b-versatile",
        input="Donne-moi un nombre entre 1 et 100",
        max_output_tokens=80
    )
```

- Aiotteko kertoa minulle: "Kyllä, yksinkertainen while-silmukka Pythonissa?" Kyllä, mutta se toimii erittäin hyvin. 2 viikossa onnistuimme saavuttamaan häikäiseviä tuloksia.

# xql.dev:n tutkimus

<h1>Rakasta tekoälyä ja matematiikkaa</h1>