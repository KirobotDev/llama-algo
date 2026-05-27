# Pochopte algoritmus `llama-3.3-70b-versatile`

- Testy byly spuštěny na několik týdnů. Viděli jsme, že systematicky odpovídá na 53 a 43 a dělá variace, ale velmi zřídka.  
To jednoduše znamená, že 90 % času používá předpřipravené odpovědi. Tak proč to dělat?  
Je to velmi dobré, ale také velmi předvídatelné. Pokud to uděláme, nemusíme vše přepisovat nebo opakovat smyčku, chcete-li.  
Díky tomu můžeme reagovat rychle, s nižšími náklady, ale problém je v tom, že neumíme inovovat.  
Pokud chceme něco nového, zkusíme vzít kousky kódu a dát je dohromady.  
Ale problém s tím je, že například nemůžeme mít slušný a inovativní frontend, protože čerpá z již vytvořených kódů :)

# Jak jsem to dokázal pochopit

- Jednoduše, vytvořil jsem malý `script` Python, který se používá k odesílání mnoha požadavků.  
Pracuje s API. Vše kromě API vám bude k dispozici.  
Toto je zhruba část kódu, která vytváří tuto smyčku odesílání:

```python
while True:
    response = client.responses.create(
        model="llama-3.3-70b-versatile",
        input="Donne-moi un nombre entre 1 et 100",
        max_output_tokens=80
    )
```

- Chceš mi říct: "Ano, jednoduchá smyčka while v Pythonu?" Ano, ale funguje to velmi dobře. Za 2 týdny se nám podařilo dosáhnout oslnivých výsledků.

# Studie od xql.dev

<h1>Miluji AI a matematiku</h1>