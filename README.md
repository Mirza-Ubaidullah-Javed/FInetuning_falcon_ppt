**# Finetuning falcon 7 billion sharded LLM to generate PowerPoint slides content in a structured way**
**## Introduction and scope:**
The repository stands as a foundation for an AI-powered app that generates PowerPoint slides for any given topic on a large domain example History, technology, literature, etc. What we have here is the building of the text part of each slide in a ppt. Note that this repository does not indulge in generating images for the slides. Rather it tunes the falcon model to generate slide content in a way that can be easily extracted and pasted into different slides using python code(This will also not be done in this repository)

**## Why Falcon?**
Falcon is a relatively new and popular LLM. It is open source and can be used from huggingface. You can check it out [here]https://huggingface.co/ybelkada/falcon-7b-sharded .It can be compared to meta's new open source LLM Llama 2. The choice between Llama and Falcon for this particular task is somewhat of a dillemma. Both yeild similar results, train in same time, and have equal helpful resource available

**## Before Fine tuning:**
![before](https://github.com/Mirza-Ubaidullah-Javed/FInetuning_falcon_ppt/assets/116464029/c5abbacd-6c55-4862-968d-2939e5b14dd6)

As you can see, the model does not do what it asked at all. It does not understand the context and rather its result is a continuation of the communication

**## Understanding the difference between fine tuning and training:**
To solve this issue we will be fine tuning falcon to give the correct output. Note that we are not training a model from scratch. Not are we providing it with data on a wide variety of topics. We are simply telling it how to understand what is being asked and yeild one the correct output and two the in the correct format

**## Data set:**
The Dataset that i have used is fairly small but sufficient. It consists of 77 files with input corresponding outputs. Each file is linked to a certain topic. 

**## Hardware Recquirements and technologies:**
+Qlora: It is important to understand that a 7 billion parameter model cannot be finetuned on a traditional machine because it recquires a lot of hardware resources. What makes this possible is Qlora, an efficient fine tuning approach that performs quantization on the weights of the model and loads them in 4 bit.
+Google colab or GPU: Using Qlora, the falcon model 7 billion can be finetuned by simple colab GPU and the 40 billion can be finetined by using the PRO subscription.
+Weights and bias: A tool that helps in the machine learning process. **Note** for fine tuning purposes, you will need a weights and biase key that you will be prompted to enter when the training begins. You can generate one [here](https://wandb.ai/authorize)

**## After Fine tuning:**
![after](https://github.com/Mirza-Ubaidullah-Javed/FInetuning_falcon_ppt/assets/116464029/f882c7b8-0629-465d-b145-38bfbe1263e9)

