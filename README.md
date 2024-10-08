



# SEMALEX 1.3.1
## Overview
SEMALEX is a cutting-edge RAG (Retrieval-Augmented Generation) Evaluation Metric designed to measure the weighted similarity score by prioritizing semantic capture while also considering lexical alignment. This metric leverages advanced NLP techniques to evaluate the quality of generated text in comparison to reference text.

## Features
**Advanced Semantic Similarity Measurement**: Leverages state-of-the-art ```Sentence Transformers``` to precisely capture and measure the semantic similarity between reference and generated text, ensuring nuanced understanding and alignment.

**Comprehensive Lexical Alignment Analysis**: Employs sophisticated ```TF-IDF(Term frequency-Inverse document frequency)``` techniques to analyze and quantify keyword overlap, providing detailed insights into lexical consistency and term relevance.

**Integrated Weighted Scoring Mechanism**: Delivers a holistic evaluation by combining ```semantic similarity``` with ```lexical alignment``` through a ```weighted scoring system```, balancing the importance of semantic capture and keyword matching for a robust and insightful assessment.
## Installation
You can install the package using pip:

```bash
pip install SEMALEX==1.3.1
```
## Usage
Here's how to use the SEMALEX Package:
```bash
from rag-evaluator import EnhancedEvaluator

# Initialize the evaluator
evaluator = EnhancedEvaluator()

# Input data
reference_text = "Human activities such as burning fossil fuels cause climate change."
generated_text = "There is a huge impact of human activities on climate. Some of these activities are burning fossil fuels, mining and so on."

# Evaluate the response
metrics = evaluator.evaluate_all(reference_text, generated_text)

# Print the results
print(f"Final Score (SemaLex): {metrics['SemaLex']}")
```

## Outcome Interpretation of SemaLex

The SemaLex evaluation metrics provide a nuanced assessment of your Retrieval-Augmented Generation (RAG) model's performance based on both lexical alignment and semantic coherence with the reference text. Below is a detailed interpretation of the outcome ranges:

### 0.0 - 0.3: Poor Performance
An outcome in this range indicates that the model's output exhibits minimal lexical alignment with the reference text and lacks semantic relevance. The response fails to capture the core meaning or context, suggesting that the model struggles with both precise term matching and contextual understanding. This reflects a fundamental deficiency in both lexical and semantic performance.

### 0.3 - 0.5: Average Performance
Scores within this range suggest that the model's output demonstrates some degree of lexical alignment with the reference text but falls short in capturing the contextual meaning. While the model may exhibit partial adherence to key terms, the overall semantic coherence is insufficient. This implies that the model's responses are somewhat consistent with the reference terms but lack the depth and diversity required for meaningful results.

### 0.5 - 0.8: Good Performance
A score in this range signifies that the model's output achieves a commendable level of both lexical and semantic alignment with the reference text. The responses not only align with the key terms but also reflect a strong contextual understanding. This indicates that the RAG model performs well in generating diverse and contextually relevant results, demonstrating a robust balance between lexical accuracy and semantic depth.

### 0.8 - 1.0: Excellent Performance
Scores in this range denote exceptional performance, where the model's output aligns nearly perfectly both lexically and semantically with the reference text. This high level of alignment reflects superior corpus diversity and an almost flawless ability to capture and replicate the nuances of the reference context. The model excels in generating responses that are both contextually rich and lexically precise, indicating optimal performance.

---

These outcome ranges provide a comprehensive evaluation of the model's capability to generate responses that are both lexically accurate and semantically meaningful, aiding in the assessment of its overall effectiveness in producing high-quality results.

## Key Components

- **`EnhancedEvaluator` Class:**  
  The cornerstone of **SemaLex**, this class integrates advanced techniques for evaluating semantic similarity and lexical alignment, providing a unified framework for comprehensive text analysis.

- **`evaluate_semantic_similarity` Method:** 
  Utilizes cosine similarity on semantic embeddings from ```Sentence Transformers``` to assess the degree of alignment between the reference and generated texts, delivering precise semantic similarity metrics.

- **`tokenize_text` Method:**  
  Employs the ```GPT-2 tokenizer``` to transform text into tokens, facilitating accurate and consistent text processing for subsequent analysis.

- **`compute_tfidf` Method:**  
  Calculates ```TF-IDF``` scores to quantify keyword relevance and distribution, enabling detailed lexical analysis and comparison.

- **`compare_keywords` Method:**  
  Analyzes and measures the overlap of ```top keywords``` between reference and generated texts, providing insights into lexical alignment and term consistency.Top keywords are selected on the basis of their TF-IDF scores thus ensuring to capture all significant words(tokens) in the texts.

- **`evaluate_all` Method:**  
  Synthesizes the results from semantic similarity and keyword overlap analyses into a final weighted score, balancing the contributions of both metrics for a holistic evaluation.

## Significance of Weighted Score

The **weighted score** in **SemaLex** represents a refined balance between semantic and lexical evaluation, encapsulating a comprehensive measure of textual similarity. This score is computed using the formula:

```python
weighted_score = (0.3 * keyword_overlap_score + 0.7 * semantic_similarity)
```


### **Semantic and Lexical Balance**

- **```Semantic Similarity (70% Weight)```:**  
  The weighted score allocates a significant 70% emphasis to semantic similarity, highlighting the importance of understanding and aligning the core meaning of the text. By employing advanced Sentence Transformers, this component focuses on the deep ```contextual relationships``` between the reference and generated texts. This approach ensures that the evaluation captures the true essence and coherence of the content, going beyond mere surface-level word matching to reflect genuine semantic alignment and contextual relevance.

- **```Lexical Alignment (30% Weight)```:**  
  Contributing 30% to the overall score, lexical alignment evaluates keyword overlap through sophisticated TF-IDF analysis. This component assesses the ```textual fidelity``` and ```consistency``` by analyzing the occurrence and relevance of specific terms between the texts. While it plays a secondary role to semantic similarity, lexical alignment is crucial for capturing the importance of terminology and its accurate representation, adding an essential layer of precision to the evaluation of textual adherence and relevance.

### **Comprehensive Evaluation**

The strategic distribution of weights ensures that the final score provides a balanced and nuanced evaluation. By combining a predominant focus on ```semantic meaning``` with an essential consideration of ```lexical accuracy```, **SEMALEX** delivers a comprehensive metric that reflects both the depth of content understanding and the precision of term usage. This ```dual-focus``` approach allows for a well-rounded assessment of text similarity, capturing both the ```substantive quality``` of meaning and the detailed ```accuracy of terminology```.




## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome!🎉 If you have any improvements, suggestions, or bug fixes, feel free to create a pull request (PR) or open an issue on GitHub. Please ensure your contributions adhere to the project's coding standards and include appropriate tests.

### How to Contribute

1. Fork the repository (Visit Github Repository: [SEMALEX](https://github.com/jhaayush2004/SEMALEX))
2. Create a new branch for your feature or bug fix.
3. Make your changes.
4. Run tests to ensure everything is working.
5. Commit your changes and push to your fork.
6. Create a pull request (PR) with a detailed description of your changes.

## Do Visit :
My Github Repository : [Ayush Shaurya Jha](https://github.com/jhaayush2004/SEMALEX)

## Contact

If you have any questions or need further assistance, feel free to reach me out via [email](shauryasphinx@gmail.com).
