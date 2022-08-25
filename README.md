# model_train

## KONKUK graduation project
### bigbird_training
* huggingface bigbird 모델 및 tokenizer 활용
  - problem
    - If input(question) enters to model, search throughout the Bible and answer.
    - At first, we used Electra, but number of tokens was limited.
    - So use Bigbird and number of tokens is increased from 512 to 4096.
  - Bigbird model architecture

![image](https://user-images.githubusercontent.com/77087144/186680051-898a9025-b4bf-4657-b7d2-6b44e542306f.png)
  
  image link : https://soundprovider.tistory.com/entry/2020-Big-Bird-Transformers-for-Longer-Sequences

### domain_classification
* huggingface bert 모델 및 tokenizer 활용
  - problem
    - If input(question) enters to model, classify which domain it is.
    - have 3 domain containing BibleQA, PlayMedia, GeneralQA
    - use BERT-base model, linear layer for classification and do fine-tuning with custom-dataset.
    - how to make custom-dataset -> link : https://github.com/syoon369/datageneration

### keyword_extraction
* huggingface distilbert 모델 및 tokenizer 활용
  - problem
    - If input(question) enters to model and is classified to PlayMedia domain or NewsSummary domain, extract keyword.
    - use SNIPS dataset and process SNIPS dataset.
    - SNIPS dataset is consisted of sentence label and token label.
    - use token label of SNIPS dataset and only use sentence which is labeled PlayMusic or SearchCreativework. Because we want to extract object of sentence and the sentences are fitted to our problem.
    - use NER(named entity recognition) method.
    - use DistilBERT to compress model.
    - post-processing is performed using output value.
  - architecture
 ![image](https://user-images.githubusercontent.com/77087144/186687350-86cf5f03-21b1-4de6-ab00-4b3b29771594.png)

