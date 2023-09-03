##### Introduction 
Purpose of this file is to provide a theoretical introduction to the entity recognition and analytical approaches used to perform it.
The notebook Entity_Resolution.ipynb describes a simple implementation of machine learning approach applied on NLP-based transformations on textual data.


**Entity recognition** 
 (also known as named entity recognition NER), is a fundamental task that involves identifying and classifying named entities within collection of various data sources (e.q. a given text or tabular data) for their deduplication (various data sources) and/or identification (mostly in the text). Named entities refer to specific words or phrases that represent real-world objects, such as persons, organizations, locations, dates, quantities, and more.


**Where can it help** </br>
In the healthcare sector, NER algorithms can assist in extracting and categorizing medical entities from clinical notes, research articles or electronic health records. </br>
In the financial industry, they can be utilized to extract and analyze information about companies, individuals, and financial transactions, helping with fraud detection, compliance monitoring and risk assessment.

Moreover, entity recognition algorithms are used in the search engines and content recommendation or classification, and they find applications in social media analysis, customer relationship management, legal document processing, news analysis, and many other fields that deal with vast amounts of textual data.

</br>

**Rule-based Approach** </br>
Rule-based systems rely on handcrafted (business) rules and patterns to identify entities, can be very tuned to the specific business application but require maintenance and manual action to detect new patterns.
</br>


**Utilizing Machine Learning** </br>
Machine learning models employ statistical algorithms to automatically learn patterns and features from labeled training data. Trained models are used to annotate raw documents identifyng entities in the text.

Particularly models utilizing deep learning, have shown remarkable quality in entity recognition due to their ability to better understand the sequential and semantic nature of the languages. Models such as recurrent neural networks (RNNs), convolutional neural networks (CNNs), and more recently, transformer-based architectures like BERT (Bidirectional Encoder Representations from Transformers), have achieved state-of-the-art performance on several NER benchmarks.


**Natural Language Processing (NLP)**</br>
NLP with tokenization and information retrival is a crucial stage preparing the input data for ML models.  

The process of entity recognition with NLP typically involves several steps: 
- Text Preprocessing: 
    - Tokenization: Breaking down the text into individual words or tokens.
    - Lowercasing: Converting all text to lowercase to ensure consistency in analysis.
    - Stopword Removal: Eliminating common words (such as "the", "and", "is") that do not carry significant meaning.
    - Stemming or Lemmatization: Reducing words to their base or root form to handle variations (e.g., "running" to "run").
- Part-of-Speech Tagging: Assigning a grammatical category (such as noun, verb, adjective) to each token in the text. Part-of-speech tagging helps in understanding the syntactic structure of the text.
- Word Embeddings: Converting words into dense numerical vectors, capturing semantic relationships between words. Techniques like Word2Vec and GloVe create these embeddings, enabling machines to understand word context and similarity.
 

**Available NER tools**</br>

- spaCy: spaCy has three main English pipelines that are optimized for CPU to perform NER - En_core_web_sm (a small size model), En_core_web_md (medium), En_core_web_lg (large).

- Stanford NER tagger:  it gives 3 main types of models - the 3-class model (to recognize organizations, persons, and locations), the 4-class model (additionaly  miscellaneous entities), the 7-class model (persons, organizations, locations, money, time, percentages, and dates). 

- NLTK: a suite of open source Python modules, data sets, and tutorials supporting research and development in NLP. It provides easy-to-use interfaces to over 50 corpora and lexical resources such as WordNet, along with a suite of text processing libraries for classification, tokenization, stemming, tagging, parsing, and semantic reasoning, wrappers for industrial-strength NLP libraries. 

- BERT: Python library provided by Google Research, source: https://github.com/google-research/bert?referral=ner-with-python

- Cloud NER engines: Lettria, Paralleldots, MonkeyLearn, Google Cloud Natural Language, Amazon Comprehend, Microsoft Azure Text Analytics, IBM Watson and other.

**Evaluation of quality of NER**
- Standard Evaluation: e.q. micro-average F1 score 
- Fine-grained analysis across buckets: 
https://www.researchgate.net/publication/347233299_Interpretable_Multi-dataset_Evaluation_for_Named_Entity_Recognition
