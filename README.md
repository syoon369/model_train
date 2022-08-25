# model_train

## KONKUK graduation project
### bigbird_training
* huggingface bigbird 모델 및 tokenizer 활용
  - problem
    - If input(question) enters to model, search throughout the Bible and answer.
    - At first, we use Electra, but number of tokens is limited.
    - So use Bigbird and number of tokens is increased from 512 to 4096.
  - Bigbird model architecture
  ![image](https://user-images.githubusercontent.com/77087144/186680051-898a9025-b4bf-4657-b7d2-6b44e542306f.png)
  image link : https://soundprovider.tistory.com/entry/2020-Big-Bird-Transformers-for-Longer-Sequences

### domain_classification
* huggingface bert 모델 및 tokenizer 활용
  - problem
    - If input(question) enters to model, classify which domain it is.
    - have 3 domain containing BibleQA, PlayMedia, GeneralQA
    - use BERT-base model and do fine-tuning with dataset.
    - how to make dataset -> link : https://github.com/syoon369/datageneration

### keyword_extraction
* huggingface distilbert 모델 및 tokenizer 활용
