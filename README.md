# Study Notes

## Metrics Overview

### What is metric?
- A metric is a quantitative measure used to evalueate the performance of an AI application.

- Helps in assessing how well the application is relatively to the given test dataset

- Provide a numerical basis for comparison, optimization and decision-making

- Essential for component selection, error diagnosis and continuous monitoring

### What are the different types of metrics?
- Metrics can be classified into two categories **based on the mechanism used underneath the hood**:
    - LLM-based metrics
    - Non-LLM-based metrics

- Metrics can be classified into two categories **based on the type of data they evaluate**:
    - Single turn metrics
    - Multi turn metrics


### What are the design principle?
- Are a set of core principles to ensure reliability, interpretability and relevance

### Explain Single-Aspect Focus principle
A single metric should target only one specific aspect of the AI application's performance

### Explain Intuitive and Interpretable principle
Metrics should be designed to be easy to understand and interpret

### Explain Effective Prompt Flows principle
When developing metrics using large language models (LLMs), use intelligent prompt flows that align closely with human evaluation

### Explain Robustness principle
Ensure that LLM-based metrics include sufficient few-shot examples that reflect the desired outcomes.

### Explain Consistent Scoring Ranges principle
It is crucial to normalize metric score values or ensure they fall within a specific range, such as 0 to 1.

## RAG Metrics

### Explain context precision
- Context Precision is a metric that measures the proportion of relevant chunks in the retrieved_contexts.

- It is calculated as the mean of the precision@k for each chunk in the context.

- Precision@k is the ratio of the number of relevant chunks at rank k to the total number of chunks at rank k.

Where K is the total number of chunks in retrieved_contexts and vk∈{0,1} is the relevance indicator at rank k.

### Explain context recall
- Context Recall measures how many of the relevant documents (or pieces of information) were successfully retrieved. It focuses on not missing important results.

### What's the difference betwen LLM recall and nonLLM recall?
- LLM Context Recall: Uses a Large Language Model (LLM) to analyze the retrieved context and compare it to the reference context. It breaks down the reference into claims and determines if each claim can be attributed to the retrieved context.

- Non LLM Context Recall: Uses non-LLM based metrics, such as string comparison, to determine if a retrieved context is relevant or not.







