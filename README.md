# LLM Task Prompting Notebook

This Jupyter notebook demonstrates how to use a small, open-source language model for various text generation tasks using the Hugging Face Transformers library.

## Overview

This project sets up a pipeline to interact with the TinyLlama-1.1B-Chat-v1.0  and another file for microsoft/Phi-3-mini-4k-instruct model, allowing users to prompt the model with various tasks and receive generated responses. It's designed to be run in environments like Google Colab, making it accessible for users without high-end local hardware.

## Features

- Easy setup and use of a pre-trained language model
- Flexible task prompting function for various text generation tasks
- Configurable generation parameters
- Examples of single-task and multi-task prompting

## Requirements

- Python 3.6+
- PyTorch
- Transformers library by Hugging Face
- (Optional) GPU for faster processing

## Setup

1. Ensure you have the required libraries installed:

```bash
pip install torch transformers
```

2. Copy the provided code into a Jupyter notebook or a Python script.

3. Run the code to set up the model and define the task prompting function.

## Usage

### Single Task Prompting

Use the `prompt_llm_task` function to give a single task to the model:

```python
task = "Explain the concept of machine learning in simple terms."
result = prompt_llm_task(task)
print(result)
```

### Multiple Task Prompting

You can also run multiple tasks in a loop:

```python
tasks = [
    "Write a short poem about artificial intelligence.",
    "Summarize the key points of climate change.",
    "Provide three tips for effective time management."
]

for task in tasks:
    print(f"\nTask: {task}")
    result = prompt_llm_task(task)
    print(f"Response: {result}")
```

## Customization

You can customize the model's behavior by adjusting the `generation_args` dictionary in the code. This allows you to control parameters like response length, randomness, and sampling strategy.

## Notes

- The TinyLlama-1.1B-Chat-v1.0 model is relatively small, which means it can run on most systems but may produce less sophisticated outputs compared to larger models.
- If you're running this in Google Colab, make sure to select a GPU runtime for better performance.
- Feel free to experiment with different prompts and tasks to explore the model's capabilities.

## Contributing

Contributions to improve the notebook or extend its functionality are welcome. Please feel free to submit issues or pull requests.

## License

This project is open-source and available under the MIT License.
