## About the Project
This Project uses meta-llama/Llama-3.2-1B model to perform supervised fine tuning, then train a reward model and then use PPO algortithm to optimise the model based on human feedback. 

Reason for Selection of model:

Recognizable and Well-Supported
The Llama family of models developed by Meta is widely recognized in the open-source AI community. Because of its popularity, it has strong ecosystem support, extensive documentation, and compatibility with many modern tooling frameworks such as Hugging Face Transformers. This makes experimentation and implementation significantly easier.

Modern Architecture
Llama 3.2 models incorporate recent improvements in transformer-based language models, providing better baseline performance compared to older models like GPT-2. Using a modern architecture ensures the project demonstrates techniques on models that reflect current industry practices.

Appropriate Size for SFT and RLHF
The 1B parameter size provides a practical balance between capability and computational efficiency. Larger models (7B–70B) require significant GPU resources, which can make training expensive and slow. The 1B model is small enough to fine-tune on limited hardware while still being powerful enough.

Efficient Experimentation
Because of its moderate size, training iterations are faster. This allows multiple experiments with different datasets, reward functions, or training configurations without excessive compute costs.

## Author
Samarth Neerkaje Saralaya