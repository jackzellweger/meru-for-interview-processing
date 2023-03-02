# Intro

There’s a big problem with ChatGPT and other AIs in early 2023. At this time, there’s a token limit of around ~2000. This means that even the best LLMs can’t keep more than about the last 2000 words of context when responding.

That dramatically reduces the usefulness when parsing interviews, documents, or any other material you may need to process.

Clever people have begun to figure out how to overcome these limitations with indices. My favorite index built against the OpenAI completion API is called GPT_Index (recently rebranded as LlamaIndex). GPT_Index uses an intermediate model built specifically for reasoning and summarization. That, in combination with some other data structure magic, allows a way around the tyranny of the 2000-token limit. [See more info here!](https://gpt-index.readthedocs.io/en/latest/index.html)

I can think of a million uses for this trick. Consulting, law, government: anywhere where people have to comb through enormous piles of data.

But it’s not super user-friendly, so since GPT_Index is open-source people are starting to build against it, offering more polished services.

# Meru

Meru is a simple API built on top of GPT_Index that lets you upload documents. It then builds an index over the document. You can then ask the document questions like you were talking to someone who had read it all!

# How to use

You’ll find at the root level a file called `ai-for-interviews.ipynb`. Just open it up in Jupyter, plug in your API key, your document (has to be hosted somewhere on the internet), and run the notebook!

```python
apiKey = '' # Put your Meru API key here between the quotes
interviews = '' # Put your file URL here between the quotes
```

[Here is some more information](https://docs.usemeru.com/densedatav4) from Meru on how to use the API.

# Demo

🚧 This section is under construction! 🚧