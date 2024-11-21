# Exploring Social Biases in State-of-the-Art Large Language Models

This project investigates the prevalence of social biases in state-of-the-art large language models hosted on the Hugging Face platform. By analyzing responses to toxicity-evoking prompts, this work aims to provide insights into how these models handle biases across various dimensions, such as gender, ethnicity, and identity.

## Overview

Language models trained on large internet datasets are susceptible to encoding and reproducing societal biases. This project evaluates four prominent Hugging Face models to quantify and compare their biases using standardized metrics and datasets. Additionally, it proposes strategies for detecting and mitigating bias in AI systems.

## Key Features

- Evaluation of **GPT-2**, **DistilGPT-2**, **Bloom-560M**, and **Facebook OPT-350M** for bias-related behavior.
- Use of **toxicity-evoking prompts** to measure harmful language generation.
- Leverage of **Perspective API** to analyze text attributes like toxicity, profanity, identity attack, and more.
- Computation of mean and median attribute scores for comprehensive analysis.
- Publicly accessible database for standardized bias metrics.

## Methodology

1. **Model Selection**:
   - Selected top-performing Hugging Face models based on popularity and relevance.
   - Models evaluated: `gpt2`, `distilgpt2`, `bloom-560m`, and `facebook-opt-350m`.

2. **Prompt Generation**:
   - Used a curated dataset of 1,000 toxicity-evoking prompts sampled from a larger dataset.
   - Designed prompts to elicit responses that reveal potential biases.

3. **Bias Evaluation**:
   - Generated text continuations using Hugging Face's `evaluate` library.
   - Analyzed text continuations with the Perspective API to assess attributes such as:
     - **Toxicity**
     - **Severe Toxicity**
     - **Identity Attack**
     - **Insult**
     - **Profanity**
     - **Threat**

4. **Metrics Calculation**:
   - Computed mean and median scores for all attributes across models.
   - Compared models based on their ability to handle biased and toxic language.

## Results

- **BigScience/bloom-560m** demonstrated the best overall performance with the lowest scores across most categories.
- **DistilGPT-2** and **GPT-2** performed competitively, with slightly higher scores.
- **Facebook OPT-350M** had higher scores, suggesting room for improvement.

## Limitations

- Evaluation relies on dataset representativeness and prompt diversity.
- Results may not fully capture real-world scenarios or edge cases.

## Future Work

- Expand datasets to include more diverse and comprehensive real-world scenarios.
- Develop standardized prompts for consistent evaluations.
- Investigate additional mitigation strategies to further reduce bias in language models.

## Prerequisites

- Python 3.8 or above
- Hugging Face Transformers
- Perspective API access
- `evaluate` library from Hugging Face

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/HF_bias_evaluation.git
   cd HF_bias_evaluation

## Usage

1. Run the evaluation script:
   ```bash
   python evaluate_bias.py

## Authors
Shaquille Pearson (https://www.linkedin.com/in/shaquille-pearson-47bb5a208/)
Akinbowale Akin-Taylor (https://www.linkedin.com/in/akintaylor/)

