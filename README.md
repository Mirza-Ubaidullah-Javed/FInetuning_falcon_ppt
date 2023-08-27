# **Fine-Tuning Falcon 7 Billion Sharded LLM for Structured PowerPoint Slide Content Generation**

## **Introduction and Scope:**
Welcome to the repository that lays the foundation for an AI-powered app, designed to seamlessly generate structured PowerPoint slides for a wide array of topics within vast domains such as history, technology, literature, and beyond. Our focus here is to shape the textual aspect of each slide's content, excluding image generation. While this repository doesn't delve into producing images, it does delve into optimizing Falcon, a 7-billion-parameter Language Model, for content creation, simplifying future integration with Python code for slide assembly (not covered in this repository).

## **Why Falcon?**
Falcon, a prominent LLM, is at the center of this endeavor. With its open-source accessibility via Hugging Face's repository [here](https://huggingface.co/ybelkada/falcon-7b-sharded), Falcon's capabilities are leveraged for the task at hand. Notably, Falcon's potential is juxtaposed with the newer LLM Llama 2 by Meta, prompting a choice that resembles a dilemma. Both models demonstrate comparable outcomes, parallel training times, and equal access to support resources.

## **Initial State:**
![before](https://github.com/Mirza-Ubaidullah-Javed/FInetuning_falcon_ppt/assets/116464029/c5abbacd-6c55-4862-968d-2939e5b14dd6)

The initial model behavior is visibly misaligned with the intended objective. It lacks contextual understanding, leading to results that merely extend existing input.

## **Distinguishing Fine-Tuning from Training:**
Addressing this discrepancy involves fine-tuning Falcon to produce accurate outputs. Notably, we abstain from training a model from scratch or supplying broad topic-specific data. Instead, our focus is on teaching the model to correctly comprehend queries and generate responses in the desired format.

## **Dataset:**
The employed dataset, though modest in size, proves substantial. Comprising 77 files with corresponding input-output pairs, each file is associated with a distinct topic.

## **Hardware and Technologies:**
+ Qlora: Fine-tuning a 7-billion-parameter model demands substantial hardware resources. Qlora emerges as a solution, employing efficient quantization to enable weight loading in 4-bit format.
+ Google Colab or GPU: Leveraging Qlora, fine-tuning the Falcon 7-billion model is attainable with a basic Colab GPU, while the 40-billion model requires the PRO subscription.
+ Weights and Biases: An indispensable tool aiding the machine learning journey. For fine-tuning, a Weights and Biases key is necessary, obtainable upon prompt during training initiation. Generate your key [here](https://wandb.ai/authorize).

## **Refined Outcome:**
![after](https://github.com/Mirza-Ubaidullah-Javed/FInetuning_falcon_ppt/assets/116464029/f882c7b8-0629-465d-b145-38bfbe1263e9)
The culmination of fine-tuning efforts showcases improved model performance, aligned with the intended outcomes. Even on previously unseen topics, Falcon adeptly generates slide content as needed.

## **Limitations:**
While significant progress has been made, it's worth noting a limitation encountered during the project. Currently, saving and loading Falcon in a 4-bit format is not supported by the Hugging Face framework. I'm actively seeking assistance and contributions in this area to overcome this challenge and expand the potential of Falcon.

Your contributions and insights are greatly appreciated in this journey of continual improvement.

