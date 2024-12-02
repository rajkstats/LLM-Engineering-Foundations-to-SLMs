<p align = "center" draggable=”false” ><img src="https://github.com/AI-Maker-Space/LLM-Dev-101/assets/37101144/d1343317-fa2f-41e1-8af1-1dbb18399719" 
     width="200px"
     height="auto"/>
</p>

<h1 align="center" id="heading">How Models Have Evolved Over Time: "How many 'r's in strawberry" 🍓</h1>


## Assignment

Over time, we've changed and improved the way we thinking about and train models in practice. 

From the earliest days of GPT, to the most recent developments like OpenAI `o1` model - model training prcoesses have undergone rapid transformation.

## So How Many 'r's are there?

Let's go through the eras of model training/post-training methods to see how things have changed with a simple question: 

`How many 'r's are in the word "Strawberry"?`

### GPT-2
Starting with [GPT2](https://cdn.openai.com/better-language-models/language_models_are_unsupervised_multitask_learners.pdf) - where pre-training was all we needed - we can see that the model doesn't even follow instructions, it's just a sequence-continuing machine.

Let's see our input: 

```
"How many 'r's are in the word "Strawberry"?"
```

And our output: 

```
"How many 'r's are in the word "Strawberry"?

The answer is, of course, no.

The word "Strawberry"
```

Let's try a model that's a bit better at following instructions.

### Llama 3 8B Instruct

Enter "Instruction Tuning". Introduced in [Cross-Task Generalization via Natural Language Crowdsourcing Instructions](https://aclanthology.org/2022.acl-long.244/), and popularized in the "FLAN paper" ([Finetuned Language Models Are Zero-Shot Learners](https://arxiv.org/abs/2109.01652)), instruction-tuning gave models the ability to follow instructions. 

Since this method was introduced, it became a staple of LLM releases, open-source or not. We'll be looking at [Meta Llama 3 8B Instruct](https://huggingface.co/meta-llama/Meta-Llama-3-8B-Instruct) to see how it gets on with our question!

We also have some additional post-training (alignment, etc.) that has been applied to make the mode respond to our instructions *how we want*.

Our input remains the same, but this time our output is: 

```
"That's a tasty question!

Let me count the "r's" for you: S-T-R-A-W-B-E-R-R-Y

There are 3 "r's" in the word "Strawberry"!"
```

Incredibly, we get the correct response!

### GenZAI - An Supervised Fine-tuned Llama 3 8B Instruct

With the advent of things like LoRA, QLoRA, and more, developers are able to leverage supervised fine-tuning to move models toward their desired behaviours - like GenZAI!

Let's ask it the same question using the supervised fine-tuned model [Gen-Z-Translate-Llama-3-Instruct-v1](https://huggingface.co/ai-maker-space/gen-z-translate-llama-3-instruct-v1):

```
"I'ma count 'em for ya! There's like, 2 "r"s in the word "Strawberry", bruh."
```

We lose correctness, but gain a GenZ flavour of speech!

### Arcee-SuperNova-v1

Next, we move on to a model that takes post-training to new heights! From alignment, to model merging, [Arcee-SuperNova-v1](https://supernova.arcee.ai/) is a juggernaut. 

Let's ask it the same question we asked the other models, and see what it says:

```
The word "Strawberry" contains two 'r's.
```

Alas, it tried its best, but didn't get there!

### OpenAI `o1`

Finally, let's stop at a model that has undergone extensive post-training (some of which we don't even know yet!) to improve reasoning capacity. 

Let's ask OpenAI's [`o1`](https://chatgpt.com/) the same question, and see what happens:

```
Thought for a couple of seconds
There are three 'r's in the word "Strawberry".
```

## Conclusion

Model training has blossomed into an entire field - which we will try to cover in our time together - in the last few years. We can finally consistently get the correct answer to life's important questions, like: 

`How many 'r's in the word "Strawberry"`
