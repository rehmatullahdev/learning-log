# Day 1: What an LLM Does (Unit 1.1)

## 1. Next-Token Prediction
* **Definition:** An LLM generates text iteratively by predicting the single most likely next token, appending it to the sequence, and repeating the process until a stop token is reached.

## 2. What an LLM Is Not
* **Not a Database / Search Engine:** It does not query structured tables or browse live records to look up stored answers. 
* **Not a Fixed Program:** It operates probabilistically through learned weights rather than following rigid, hardcoded programmatic rules.

## 3. The Path Through the Model
1. **Tokenization:** Raw text input is split into smaller chunks called tokens.
2. **Numerical Conversion:** Tokens are converted into numerical representations (vectors/IDs) that the model's architecture can process.
3. **Layer Refinement:** Deep neural network layers process and refine these numbers, capturing context, syntax, and semantics.
4. **Probability Distribution:** The model outputs a probability score across its vocabulary for the likelihood of each possible next token.

## 4. Understanding Parameter Counts
* **Scale (e.g., 8B vs. 70B):** Parameter counts represent the size of the model's learned weights (what it has memorized and generalized during training) .
* **Capability vs. Efficiency:** While higher parameter counts generally correlate with higher capacity and nuance, bigger is not automatically better; smaller models can be faster, cheaper, and fine-tuned to outperform larger ones on specific tasks .

## 5. Why Chat Models Behave as They Do
* **Instruction & Feedback Tuning:** Base models are trained only to predict the next word on raw internet text. Chat models undergo additional training phases (like RLHF - Reinforcement Learning from Human Feedback) to learn how to:
  * Follow user instructions 
  * Maintain a conversational persona 
  * Refuse harmful requests safely 
  * Hedge uncertain answers