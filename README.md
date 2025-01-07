# Entity Recognition Using an LLM API

This repository provides an overview of a project designed for a class, where an **LLM API** was prompted for the task of **entity recognition**. The project focuses on effectively interacting with a language model API to identify entities in text, while exploring the impact of different demonstration modes and shot variations on model performance.

> **Note:** The exact implementation code is not provided here, but if you're interested in discussing the project or seeing specific details, feel free to reach out to **anirudhm@andrew.cmu.edu**!

---

## Project Overview

The project leverages the **GPT-4o-mini** model. Key objectives include:
- Designing functions to format input data into structured messages for the model.
- Implementing functions to maintain and return chat history for iterative interactions.
- Experimenting with diverse demonstration modes to understand their impact on model performance across various settings, particularly focusing on metrics such as **F1 score, precision**, and **accuracy**.

---

## Key Features

1. **Supporting Libraries**:
   - **OpenAI**: For interfacing with the LLM API.
   - **PyTorch**: For handling data and conducting experiments.
   - **`re` library**: For preprocessing and pattern matching in text.

2. **Input Formatting**:
   - Implemented a function to transform examples from the dataset into a structured message format compatible with the LLM's expected input.

3. **Chat History Management**:
   - Developed a function to maintain and return the conversation history, enabling contextual interactions.

4. **Demonstration Modes**:
   - Conducted experiments with three distinct demonstration modes:
     - **Random**:
       - Selected 42 random examples from the dataset as demonstrations.
       - The goal was to provide a general but unstructured set of inputs to the model.
     - **Diverse**:
       - Filtered examples based on their labels to ensure a wide variety of inputs.
       - The idea here is that the breadth of inputs helps the model adapt more strongly to patterns in the test set.
     - **Complex**:
       - Selected examples with the most complicated sentence structures, often corresponding to longer sentences.
       - The idea is to better train the model to deal with complex patterns, making it more adept at handling similarly complicated inputs in the test set.

6. **Shot Variation Analysis**:
   - Varied the number of demonstrations (shots) to study the impact on performance.
   - Few-shot, medium-shot, and many-shot setups were analyzed to identify optimal configurations for performance.

7. **Performance Metrics**:
   - Evaluated the model's entity recognition capabilities using established metrics, focusing on **F1 score**, which measures a model's accuracy by combining its precision and recall scores.

---

## Acknowledgments

A special thanks to the instructors of my NLP course, Professors David Mortensen and Eric Nyberg, for their invaluable guidance on this project.

---

For inquiries or collaboration opportunities, feel free to reach out to **anirudhm@andrew.cmu.edu**!
