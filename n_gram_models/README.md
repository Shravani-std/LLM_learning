You can write it in your README like this:

---

# Model Comparison and Constraints

## Response Time Requirements

The response time of the language model should be fast enough for real-time text generation and prediction tasks.

* **Unigram Model:** Fastest response time because it predicts based on single-token probabilities only.
* **Bigram Model:** Moderate response time since it considers one previous token.
* **Trigram Model:** Slightly slower because it processes two previous tokens and requires more computations.

In mobile or low-resource devices, the inference time should ideally remain below a few milliseconds per prediction for smooth user interaction.

---

# Quality of Suggestions

The quality of generated text improves as the context size increases.

| Model   | Context Used      | Quality  |
| ------- | ----------------- | -------- |
| Unigram | No context        | Poor     |
| Bigram  | 1 previous token  | Moderate |
| Trigram | 2 previous tokens | Better   |

### Observations

* **Unigram Model**

  * Generates random and incoherent text.
  * Cannot capture sequence relationships.

* **Bigram Model**

  * Learns local character/word transitions.
  * Produces more meaningful outputs than unigram.

* **Trigram Model**

  * Captures short contextual dependencies.
  * Produces more coherent and realistic text generation.

Generally, trigram models provide better prediction accuracy and lower perplexity compared to unigram and bigram models.

---

# Memory Constraints on Mobile Devices

Memory usage increases with context size and model complexity.

| Model   | Memory Usage | Mobile Suitability |
| ------- | ------------ | ------------------ |
| Unigram | Very Low     | Excellent          |
| Bigram  | Low          | Good               |
| Trigram | Moderate     | Acceptable         |

### Memory Considerations

* Mobile devices have limited:

  * RAM
  * Storage
  * Battery power

* **Unigram models** require minimal memory and computation.

* **Bigram models** require additional storage for transition probabilities or neural parameters.

* **Trigram models** consume more memory due to:

  * Larger embedding representations
  * Increased parameter count
  * Higher computational requirements

For resource-constrained mobile systems:

* smaller embedding sizes,
* quantization,
* and lightweight architectures

can help reduce memory consumption.

---

# Overall Tradeoff

| Model   | Speed     | Memory   | Quality |
| ------- | --------- | -------- | ------- |
| Unigram | Very Fast | Very Low | Low     |
| Bigram  | Fast      | Low      | Medium  |
| Trigram | Moderate  | Moderate | Better  |

The choice of model depends on the application requirements between:

* speed,
* memory efficiency,
* and text generation quality.
