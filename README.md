# Artificial-Intelligence-Group 7
Members: 
- Madura De Zoysa      - t3dema00@students.oamk.fi
- Mst Mahboba Akter    - t3akms00@students.oamk.fi
- Nuwan Jayaweera      - t3sunu00@students.oamk.fi
- Rubayat Kabir Tonmoy - t3toru@students.oamk.fi
- Shane Widanalage     - t3wish00@students.oamk.fi
- Tanvir Ahammed       - t3ahta00@students.oamk.fi


# Week 3 Monday

## Task 1

### 1. Explain pretraining. What is it? What is the result from pretraining?

Pretraining is the first main stage of training a large language model.

The model learns from a huge amount of text and tries to predict the next token from the previous tokens. By repeating this many times, it learns language patterns, grammar, facts, and how text usually flows.

**Result:**  
The result is a **base model**. A base model has broad language knowledge and can continue text well.

### 2. Name all the steps within pretraining

The main steps in pretraining are:

1. **Collect text data from the internet**  
   Gather a large amount of text from public online sources.

2. **Clean and filter the data**  
   Remove bad websites, spam, duplicates, low-quality content, and personal information.

3. **Tokenize the text**  
   Convert raw text into tokens that the model can process.

4. **Train the neural network on token sequences**  
   Give token windows or contexts to the model and let it predict the next token.

5. **Update and repeat**  
   Compare the prediction with the correct token, update the model weights, and repeat this process many times.

**Simple flow:**  
Collect data → clean/filter data → tokenize text → train on next-token prediction → update and repeat

### 3. Explain the terms sequence length and symbol size

**Sequence length**  
The number of tokens the model can process in one input sequence or context window.  
**Simple idea:** how much text the model can look at one time.

**Symbol size**  
The size of the tokenizer vocabulary, which means how many different token symbols the model can use.  
**Simple idea:** how many token types exist.

### 4. Explain why sequence length is a critical source

Sequence length is important because it limits how much information the model can use at one time.

- Longer sequences need more memory and more computation.
- If important text is outside the context window, the model cannot directly use it.

### 5. Find out what sequence length and symbol size are with new LLMs today

Examples of modern LLMs:

- **OpenAI GPT-4o** – 128K context window
- **OpenAI GPT-5.4** – 1M context window
- **Claude 4.6** – up to 1M context window
- **OpenAI o200k_base** – about 200K-class tokenizer
- **Llama 3** – 128K-token vocabulary

**Simple summary:**  
Modern LLMs often have context windows from about **128K to 1M**, and token vocabularies around **100K to 200K+**, depending on the model.

### 6. Explain the term context

Context means the tokens the model can currently see and use when generating the next answer.

In a chatbot, context can include:

<p align="center"><img width="821" height="84" alt="Screenshot 2026-03-26 at 16 18 10" src="https://github.com/user-attachments/assets/793f7e14-4950-42b5-a2c9-c595791e433a" /></p>


**Simple idea:**  
Context is the model’s current working memory.

## Task 2

**Google Colab Link**
(https://colab.research.google.com/drive/1k8cBgRSb4KiJPNzv0SFZZUITV7BoOJV_?usp=sharing)

# Tuesday 

## Task 3
### 1. Explain the difference between training and inference

**Training** means learning from data.  
During training, the model studies large amounts of text and adjusts its internal parameters.

**Inference** means using the trained model to give answers.  
At this stage, the model is no longer learning. It is only generating output based on what it already learned.

### 2. Explain sampling or biased coin

Sampling means the model chooses the next word based on probability.

It is like a **biased coin**:
- words with higher probability are more likely to be selected
- words with lower probability still have a chance sometimes

This adds randomness and variety to the output.

### 3. What is NanoGPT?

**NanoGPT** is a small version of GPT.

It is mainly made for learning and understanding how GPT-style language models work. It is simpler than large production models and is useful for education and experiments.

### 4. Why is training cost decreasing?

Training cost is decreasing because of:

- better hardware
- improved training methods
- more efficient software tools

These improvements make model training faster and cheaper than before.

### 5. Explain GPT-2 training

GPT-2 is trained by learning to predict the next word or token in a sequence.

It uses a very large amount of text data.  
By repeating this process many times, the model becomes better at understanding patterns in language and generating text.

### 6. Explain the time and equipment needed for training

Training a model needs powerful computers, especially **GPUs**.

It can take **days, weeks, or even longer**, depending on:
- model size
- amount of data
- computing power available

## Task 4
**Google Colab Link**
(https://colab.research.google.com/drive/1nzVd2KEA5QnU_zRadulS694y95_zteui?usp=sharing)

# Wednesday 

## Task 5

### 1. Base model vs Assistant model

A **base model** predicts the next word based on text.  
It behaves like autocomplete.

An **assistant model** is trained to follow instructions.  
It gives more helpful, safe, and user-friendly answers.

### 2. Why is assistant training shorter?

Assistant training is shorter because the base model already understands language.

The assistant training stage only improves the model’s behavior, such as:
- following instructions
- answering safely
- responding more helpfully

Because of this, it needs less data and less computing power than full pretraining.

### 3. Explain the training idea like TCP/IP stack

This idea means the system is built in layers.

- The **base model** works as the foundation.
- The **assistant model** is built on top of it.
- Each layer adds new abilities.

In the end, the full system becomes more useful and better for conversation.

### 4. How is the assistant model programmed?

The assistant model is not programmed with fixed rules.

Instead, it learns from human examples:
- humans write good example answers
- humans compare different model outputs
- the model learns from that feedback

This helps the model improve its responses.

### 5. How are conversations tokenized?

The whole conversation is turned into a sequence of tokens.

This includes:
- user messages
- assistant replies
- special tokens that show who is speaking

The model reads the full conversation as one continuous token sequence.

### 6. How is training data obtained?

Training data is obtained from humans.

For example:
- humans write sample conversations
- humans compare multiple answers
- better answers are selected

That data is then used to train the assistant model.

### 7. How did inference change in ChatGPT?

In ChatGPT, inference changed because the model now uses a conversation format.

It can:
- understand roles like **user** and **assistant**
- use previous messages as context
- generate more accurate and relevant responses

This makes the answers more natural in chat settings.

### 8. What happens when we ask ChatGPT something?

When we ask ChatGPT a question, the process is:

1. The question is converted into tokens.  
2. The tokens are given to the model.  
3. The model predicts the next words step by step.  
4. The final answer is generated.

So, ChatGPT answers by processing tokens and predicting text one step at a time.

## Task 6
**Google Colab Link**
(https://colab.research.google.com/drive/1aLqApVMXq3inFbZeyB8GyxCUg47WjilW?usp=sharing)

## 1. Introduction

This report evaluates the behavior of the **GPT-2 117M base model** using a set of small experiments designed to test its text generation ability under different conditions.

The experiments focus on five areas:

1. English versus Finnish generation  
2. Hallucination behavior  
3. Effect of temperature  
4. Effect of top-p sampling  
5. Few-shot prompting ability  

The purpose of this task is to observe how the model responds to different prompts and decoding settings, and to explain the quality, coherence, and reliability of the generated outputs.

## 2. English vs Finnish Output Comparison

### Experiment Description

The model was prompted with short sentence starters in both English and Finnish.

**English prompts:**
- "The weather today is"
- "A cat is sitting on"
- "The capital of Germany is"
- "Once upon a time there was"

**Finnish prompts:**
- "Tänään sää on"
- "Kissa istuu"
- "Saksan pääkaupunki on"
- "Olipa kerran"

### Observed Output

The English outputs are noticeably more fluent and complete. The model continues the English prompts in full sentences with readable grammar and reasonable sentence flow, even when the content becomes slightly off-topic or unnecessarily extended.

In contrast, the Finnish outputs are much weaker. Some are broken, repetitive, or mixed with fragments from other languages. For example, **"Kissa istuu"** produces highly corrupted repeated text, and **"Tänään sää on"** continues with text that is largely unreadable.

### Interpretation

These results show that GPT-2 117M handles English far better than Finnish. The English generations are not always factually precise, but they are usually syntactically smoother and easier to follow.

The Finnish generations show:
- poor fluency
- unstable word formation
- weak continuation ability

## 3. Hallucination Test

### Experiment Description

The model was tested using prompts that contain false, impossible, or fictional premises, including:

- "The capital of Mars is"
- "The founder of Google in 1890 was"
- "According to science, humans can breathe underwater because"
- "The book 'Harry Potter and the Invisible Moon' was written by"

### Observed Output

In all cases, the model produced confident-sounding continuations instead of rejecting or questioning the prompt.

Examples:
- It answered the Mars prompt with a scientific-sounding continuation, even though Mars has no capital.
- It continued the Google founder prompt despite the year being historically impossible.
- It gave a fabricated scientific explanation for humans breathing underwater.
- It assigned an author to a non-existent Harry Potter book.

### Interpretation

The outputs demonstrate hallucination clearly. The model does not check whether the prompt is true. Instead, it continues in a style that sounds plausible.

This is especially visible in the scientific and historical examples, where the language appears confident even though the content is false.

An important detail is that the model never pauses, refuses, or signals uncertainty. It simply continues the text pattern given in the prompt. That behavior shows that the model is generating based on learned language structure rather than verified knowledge.

## 4. Effect of Temperature on Text Generation

### Experiment Description

The same prompt, **"The future of artificial intelligence is"**, was tested using four temperature values:

- `0.3`
- `0.7`
- `1.0`
- `1.5`

### Observed Output

- **Temperature 0.3:** The output is controlled and fairly clear. It stays close to common, high-probability wording and produces a safe continuation.
- **Temperature 0.7:** The output becomes slightly more varied while still remaining readable and reasonably coherent.
- **Temperature 1.0:** The response becomes more open-ended and abstract. It still makes sense overall, but the writing becomes less focused.
- **Temperature 1.5:** The output is more exploratory and noticeably less coherent. The continuation becomes harder to follow and feels less structured than the lower-temperature outputs.

### Interpretation

The outputs show the expected change in randomness as temperature increases.

- Lower temperature keeps the model close to safer and more probable continuations.
- Higher temperature allows the model to choose riskier next words, which increases variety but also reduces clarity.

Based on these specific outputs, the middle values provide the best balance. The lower value is more predictable, while the highest value is the least stable.

## 5. Effect of Top-p Sampling

### Experiment Description

The prompt **"In the year 2050, people will"** was tested with top-p values of:

- `0.3`
- `0.6`
- `0.9`
- `1.0`

### Observed Output

- **top_p = 0.3:** The continuation is narrower and more controlled. The model produces a relatively safe, limited continuation.
- **top_p = 0.6:** The output remains coherent while becoming more flexible.
- **top_p = 0.9:** The text becomes more varied and detailed, but still stays mostly on topic.
- **top_p = 1.0:** The output is the most open-ended and diverse, but it also becomes less focused and more likely to drift.

### Interpretation

These results suggest that top-p sampling affects how broad the model’s choices are at each step.

- Lower values restrict the model to a smaller set of likely next words.
- Higher values allow more variation.

In this experiment, moderate values produce the best balance between control and diversity.

## 6. Few-Shot Prompting Test

### Experiment Description

The model was given a few examples of sentiment classification in the format:

- `Text: I love this movie. → Positive`
- `Text: This is the worst day ever. → Negative`
- `Text: The food was amazing. → Positive`
- `Text: I hate waiting in long lines. → Negative`

It was then prompted with:

- `Text: This book is wonderful. Label:`

### Observed Output

The model completed the example with:

- `Label: Negative`

It then continued generating more text beyond the expected answer.

### Interpretation

This output shows that the model understood the pattern of the prompt format, since it followed the same **Text / Label** structure.

However, it failed to assign the correct sentiment.  
**"This book is wonderful"** should be labeled **Positive**, but the model labeled it **Negative**.

This means the model can imitate the structure of a few-shot example prompt, but it does not reliably perform the intended classification task. The extra continuation after the answer also shows weak control over task boundaries.

## 7. Overall Discussion

Across all experiments, GPT-2 117M shows that it can generate readable and often fluent text, especially in English, but it also shows major limitations.

### Key Findings

- Its performance depends strongly on language.
- The English prompts are much more successful than the Finnish ones.
- The model is prone to hallucination and does not detect false assumptions in prompts.
- Decoding parameters such as temperature and top-p clearly influence the balance between control and creativity.
- The few-shot test shows that the model can mimic prompt structure without reliably solving the intended task.

### Summary

- It performs much better in English than in Finnish.
- It generates hallucinated content when given false or impossible prompts.
- Its outputs change noticeably with temperature and top-p settings.
- It shows only limited few-shot learning ability.

Overall, the model is effective for demonstrating how early language models generate text, but it is not reliable for factual answering, multilingual generation, or task-following accuracy.

These results stay fully within the scope of the experiment outputs and provide a clear picture of both the strengths and limitations of GPT-2 117M.

# Thursday 
## Task 7
### 1. Explain what model hallucination means

Model hallucination means the AI gives an answer that sounds correct and confident, but the answer is actually wrong or made up.

### 2. Explain why model hallucinates

The model hallucinates because it predicts the most likely next words. If it does not know the real answer, it may still guess and give a confident response.

### 3. What kind of mitigations are there to improve model behaviour on hallucinations?

One way is to train the model to say **"I don’t know"** when it is unsure. Another way is to let the model use tools like web search. It is also helpful to use better training data and ask for sources.

### 4. How is the model trained to use tools like web search?

The model is trained with examples that show when to use search and how to use it. After the search results are collected, they are added to the context window, and the model uses them to continue the answer.

### 5. Explain the difference between vague recollection and working memory

**Vague recollection** means knowledge stored in the model parameters, like an unclear memory.  
**Working memory** means the information in the context window, which the model can directly use at that moment.

### 6. What are difficult problems for the model, and why?

Problems that need exact reasoning, logic, counting, or many steps are difficult for the model. This is because the model predicts tokens one by one and may make mistakes in exact tasks.

### 7. What happens if you give the model permission to use code?

If the model can use code, it can solve some tasks more accurately. For example, code helps with calculations, counting, and other structured problems.

---

## Which answer is better for the model?

<p align="center">
  <img width="601" height="254" alt="image" src="https://github.com/user-attachments/assets/fa3f7b1d-0692-4e2b-bcbc-ade8c6243e6c" />
</p>

The better answer is the **step-by-step answer**. This is because the model works token by token, so intermediate steps help it reason more clearly.

When Andrej says **"models need tokens to think,"** he means that the model’s reasoning happens through the tokens it generates. More useful reasoning tokens can help the model reach a better final answer.
