This repository contains datasets for two NLP tasks: **Complex Word Identification (CWI)** and **Lexical Simplification (LS)** for Persian.

Here's a breakdown of the files:

### CWI_gold_ds.csv

This is the gold standard dataset for Complex Word Identification for Persian. Each row contains a target word, its context, and human-provided complexity labels.

* **word**: The target word.
* **sentences**: The sentence in which the target word appears.
* **majority voted complexity label**: A binary label indicating whether the word is non-complex (0) or complex (1) based on a majority vote from 5 annotators.
* **complex_percentage**: The percentage of annotators who labeled the word as complex.
* **str_idx**: The starting index of the target word in the sentence.
* **end_idx**: The ending index of the target word in the sentence.

### LS_gold_ds.csv

This is the gold standard dataset for Lexical Simplification evaluation using SARI and BLEU metrics. It provides original sentences containing complex words and two simplified versions, by two human linguists, for each.

* **Original_sentence**: The original sentence.
* **simplified_1**: The first simplified version of the sentence.
* **simplified_2**: The second simplified version of the sentence.

### sample_0_complexity_feature.csv & sample_1_complexity_feature.csv

These two files contain 6k words each and selected complexity features. `sample_0` contains non-complex words, and `sample_1` contains complex words. These are feature sets for training a rule based CWI model.

* **target_word**: The word.
* **freq**: The frequency of the word in a corpus (Miras and Bijankhan corpora).
* **LenChar**: The length of the word in characters.
* **VowConRatio**: The ratio of vowels to consonants in the word.
* **label**: The complexity label (0 for simple, 1 for complex).
