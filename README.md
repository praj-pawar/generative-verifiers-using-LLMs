# stepwise DPO trainer with LLM-based reward model

this project implements stepwise direct preference optimization (DPO) using an LLM as a stepwise reward model. 
<br>
the goal is to train a model that learns to solve problems by evaluating reasoning steps, utilizing an LLM to automatically assess the quality of each step.

## Features

- [x] use of LLM as a stepwise reward model: the implementation uses a large language model (LLM) to evaluate and score each step in the problem-solving process. instead of human feedback, the llm provides reasoning and assigns scores, making it possible to automate the evaluation process.
  
- [x] stepwiseDPOtrainer class: a custom trainer class is implemented by inheriting from Hugging Face’s DPOTrainer, with modifications to handle stepwise reasoning and LLM-based rewards. this trainer computes stepwise rewards, comparing "chosen" and "rejected" completions to train the model.

- [ ] small model support: the stepwise DPO training can be applied to small models as well. I provide an efficient setup using **LoRA (Low-Rank Adaptation)**, which enables fine-tuning of large models with a reduced parameter count, making the process faster and more efficient for limited resources.
