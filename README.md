# Love Ai Study

<img src="./md/look.gif" alt="une fille eclairer par du vert qui regarde un écrans de pc on vois le reflet dans sais lunette" />


# Code (Help Ai for write in files) :)

```python
import json
import os
import re
from openai import OpenAI
from key import key

client = OpenAI(
    api_key=key,
    base_url="https://api.groq.com/openai/v1",
)

file_name = "resultats.json"

if os.path.exists(file_name):
    try:
        with open(file_name, "r", encoding="utf-8") as f:
            data = json.load(f)

            if not isinstance(data, list):
                data = []

    except:
        data = []
else:
    data = []

while True:
    response = client.responses.create(
        model="llama-3.3-70b-versatile",
        input="Donne moi un nombre entre 1 et 100",
        max_output_tokens=80
    )

    texte = response.output_text
    print(texte)

    nombre = int(re.search(r"\d+", texte).group())

    data.append(nombre)

    with open(file_name, "w", encoding="utf-8") as f:
        json.dump(data, f, indent=4, ensure_ascii=False)

    print("Ajouté :", nombre)
```
