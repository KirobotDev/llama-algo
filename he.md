# Comprendre l'algo `llama-3.3-70b-versatile`

- Les tests sont lancés depuis quelques semaines. Nous avons pu voir qu'il répond systématiquement 53 et 43, et fait des variantes, mais très rarement.  
Cela veut simplement dire qu'il utilise 90 % du temps des réponses préenregistrées. Alors pourquoi faire ça ?  
C'est très bien, mais aussi très prévisible. Si on fait ça, on n'a pas besoin de tout réécrire ni de refaire la boucle, si vous préférez.  
Du coup, on peut répondre vite, à moindre coût, mais le problème, c'est qu'on ne peut pas innover.  
Si on veut quelque chose de nouveau, ça va essayer de prendre des bouts de code et les assembler.  
Mais le problème avec ça, c'est qu'on ne peut pas, par exemple, avoir un frontend potable et innovant, car ça pioche dans des codes déjà faits :)

# Comment j'ai réussi à comprendre

- Simplement, j'ai créé un petit `script` Python qui sert à envoyer plein de requêtes.  
Ça marche avec l'API. Tout sera à votre disposition sauf l'API.  
Voilà en gros la partie du code qui crée cette boucle d'envoi :

```python
while True:
    response = client.responses.create(
        model="llama-3.3-70b-versatile",
        input="Donne-moi un nombre entre 1 et 100",
        max_output_tokens=80
    )
```

- Vous allez me dire : "Oui, une simple boucle while en Python ?" Eh oui, mais ça marche très bien. En 2 semaines, nous avons réussi à avoir des résultats fulgurants.

# Étude par xql.dev

<h1>Love AI & math</h1>
