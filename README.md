# LORuGEC
**Linguistically Oriented Rule-annotated GEC dataset for Russian**
* **Sentences representing the rules of Russian grammar that are complicated both for L1 learners and LLMs.**
* Rules were adopted from various resources, such as grammar reference books, teacher manuals and educational websites based on them. The textbooks that were used comply with Russian educational standards, some of them are specially approved by the Russian Academy of Sciences.
* Novel methodology of data collection: the annotators, which were students with linguistic backgrounds & Russian native speakers, selected sentences for each rule and inserted corruptions manually. Afterwards, the sentences were passed through a LLM and lists of sentences for complicated rules were further extended.
* In total, there are 48 rules from 4 grammar sections in LORuGEC, majorly punctuation and spelling.
* Our corpus is deliberately created for evaluation and diagnostic purposes. Therefore, it has no training subset and is much smaller than other GEC corpora.  We don't want LLMs to acquire new capabilities on the validation set of our corpus, but rather to reveal the knowledge they already have.

## Data Format
* LORuGEC.xlsx
  
  The dataset consists of rules, their definitions, information on their complexity for the YandexGPT model, pairs of corresponding tokenized grammatical and ungrammatical sentences. There is some additional information, representing grammar sections which rules pertain to, sources of rules as well as indication of the subset for each sentence (validation or test). There are few sentences in the dataset that do not contain any errors, because it is also crucial to verify if models are prone to hypercorrection. These sentences are also marked with metadata.
* We also present our data in .M2, which is a conventional GEC format. According to the .M2-standard, the source text is denoted with *S*, while the corresponding edits are prefixed with *A*. Each edit consists of the error span, error type, correction, if the edit is optional or required, additional remarks and annotator ID, yet we don't make use of error types.

# :boom: Cite us
LORuGEC is introduced in the paper **LLMs in alliance with Edit-based Models: Advancing In-Context Learning for Grammatical Error Correction by Specific Example Selection** accepted to the [BEA 2025 Workshop](https://sig-edu.org/bea/2025) at the [ACL 2025 Conference](https://2025.aclweb.org/).

If you use LORuGEC in your research, please cite:
```
Sorokin, A., Nasyrova, R. LLMs in alliance with Edit-based Models: Advancing In-Context Learning for Grammatical Error Correction by Specific Example Selection
```
