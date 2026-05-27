# Understand the `llama-3.3-70b-versatile` algorithm

- The tests have been launched for a few weeks. We could see that he systematically answers 53 and 43, and makes variations, but very rarely.  
This simply means that it uses canned responses 90% of the time. So why do this?  
It's very good, but also very predictable. If we do that, we don't need to rewrite everything or redo the loop, if you prefer.  
As a result, we can respond quickly, at lower cost, but the problem is that we cannot innovate.  
If we want something new, we'll try to take pieces of code and put them together.  
But the problem with that is that we can't, for example, have a decent and innovative frontend, because it draws on codes already made :)

# How I managed to understand

- Simply, I created a little `script` Python which is used to send lots of requests.  
It works with the API. Everything will be at your disposal except the API.  
This is roughly the part of the code that creates this send loop:

```python
while True:
    response = client.responses.create(
        model="llama-3.3-70b-versatile",
        input="Donne-moi un nombre entre 1 et 100",
        max_output_tokens=80
    )
```

- Are you going to tell me: "Yes, a simple while loop in Python?" Yes, but it works very well. In 2 weeks, we managed to achieve dazzling results.

# Study by xql.dev

<h1>Love AI & math</h1>