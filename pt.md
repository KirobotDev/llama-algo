# Entenda o algoritmo `llama-3.3-70b-versatile`

- Os testes foram lançados há algumas semanas. Pudemos perceber que ele responde sistematicamente 53 e 43, e faz variações, mas muito raramente.  
Isso significa simplesmente que ele usa respostas predefinidas 90% do tempo. Então, por que fazer isso?  
É muito bom, mas também muito previsível. Se fizermos isso, não precisaremos reescrever tudo ou refazer o loop, se preferir.  
Como resultado, podemos responder rapidamente, com custos mais baixos, mas o problema é que não podemos inovar.  
Se quisermos algo novo, tentaremos pegar pedaços de código e juntá-los.  
Mas o problema disso é que não podemos, por exemplo, ter um frontend decente e inovador, porque ele se baseia em códigos já feitos :)

#Como consegui entender

- Simplesmente, criei um pequeno `script` Python que é usado para enviar muitas solicitações.  
Funciona com a API. Tudo estará à sua disposição exceto a API.  
Esta é aproximadamente a parte do código que cria este loop de envio:

PROTEGER_0

- Você vai me dizer: "Sim, um loop while simples em Python?" Sim, mas funciona muito bem. Em 2 semanas, conseguimos resultados deslumbrantes.

# Estudo por xql.dev

<h1>Adoro IA e matemática</h1>