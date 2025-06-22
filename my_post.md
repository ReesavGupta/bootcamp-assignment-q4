# Hallucinations: Bug or Feature?

You have misunderstood hallunicination in AI. I'm going to explain what it is, what we get wrong, and why this is stopping you from getting the most value out of AI today.

## What Even Is a Hallucination
 
This is the term we use when ai just makes something up on its own. For example,  there was a case when a lawyer used chatgpt to cite fake cases in a legal breif(https://www.legaldive.com/news/chatgpt-fake-legal-cases-generative-ai-hallucinations/651557/). The lawyer got into trouble for not bothering check, if the thing that ai had found was not real at all. So it just made it up. it looked real but nope. it wasnt.

If you are a sofware developer like me, you have probably been using AI coding assistants, something like github copilot, and you will almost have had had the experiece where you tell it to write some code for you. It gives you something which looks great. You have a look over it. Yes! it looks exactly like what i wanted it to be, great! Only to find out, it doesnt work. Because, it tried to use API that does not actually exist.

So, the broad thing to notice here is that the AI will sometimes just come up with something that seems completely reasonable, but which turns out to have made up. That is what we describe as hallcination.

## Why Calling It a Bug Might Be the Real Problem

Now, hallucination is a colorful term, but i think it is problematic. The problem with calling it hallucination is that, it makes it sound like a bug, as a problem, a mistake. 
And im gonna argue that, when you fully understand what is happening when AI hallucinates, you'll realize that's not what they are doing. And actually that behavior is the main value that the AI's today have to offer.
Now that might sound like a mad statement. Like why on earth would I be calling this behavior where the AI makes up things a feature? How's that useful ? How can I not be calling that a bug ? But a feature.

Well, i think the key here is to think that, why it does what it does and why that is actually a matter just the manner in which ai has to offer. If you are designing ai based systems or even if you are using ai, its useful for what it really does. I think your life will be better if you accpet what it is that AI's do. Because you will be able to design better solutions that will be able to work with it rather that going against the fundamental nature.

## Why AI "Hallucinates"

LLM's like GPT-4, claude, gemini are trained using unsupervised learning. These models are fed lots and lots of data, like actually alot of data. The core objective is to understand the patterns and relationships in the data without any specific guidance on what to learn. To predict the next token (word or subword) given a seques of previous tokens.

This means that they dont know facts. They learn patterns and statistic relations. So when it doesn’t have the right info, it will fill the blanks with something that sounds correct, but isn’t.

Here is an example: 

```python
import openai

openai.api_key = "your-api-key"

response = openai.ChatCompletion.create(
  model="gpt-3.5-turbo",
  messages=[{"role": "user", "content": "What chemical element has the symbol 'Ht'?"}]
)

print(response['choices'][0]['message']['content'])
```
There is no chemical element with the symbol HT. But depending on how you ask, the model might still invent an answeer because that is what they are trained to do.

## When Hallucination is a Feature

Thus to summarize 
Hallucinations becomes a feature when the task is creativity, idea genaration or language generation, not the acccuracy of the result.
