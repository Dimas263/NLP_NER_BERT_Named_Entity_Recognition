# NLP - BERT Named-Entity Recognition

# Architecture

<img src="NER%20Architecture.png">

# [Dataset](input/ner_dataset.csv)

| Sentence #  | Word        | POS | Tag     |
| ----------- | ----------- | --- | ------- |
| Sentence: 0 | studies     | NNS | O       |
| Sentence: 0 | on          | IN  | O       |
| Sentence: 0 | magnesium   | NN  | O       |
| Sentence: 0 | s           | NN  | O       |
| Sentence: 0 | mechanism   | NN  | O       |
| Sentence: 0 | of          | IN  | O       |
| Sentence: 0 | action      | NN  | O       |
| Sentence: 0 | in          | IN  | O       |
| Sentence: 0 | digitalis   | NN  | plant   |
| Sentence: 0 | induced     | VBD | O       |
| Sentence: 0 | arrhythmias | NNS | disease |
...

# Labels

```yaml
{'O': 0, 'disease': 2, 'plant': 1}
```

# Config

```yaml
MAX_LEN = 300
TRAIN_BATCH_SIZE = 8
VALID_BATCH_SIZE = 4
EPOCHS = 10
LEARNING_RATE = 1e-05
MAX_GRAD_NORM = 10
```

# Tokenizer And Model

```yaml
git clone https://huggingface.co/dmis-lab/biobert-v1.1
```

# Scores

| Entities     | precision    | recall       | f1-score     |
| ------------ | ------------ | ------------ | ------------ |
| O            | 0,9734890619 | 0,9767485119 | 0,9751160631 |
| disease      | 0,8463157895 | 0,7686424474 | 0,8056112224 |
| plant        | 0,8722358722 | 0,9416445623 | 0,9056122449 |
| accuracy     | 0,9572976418 | 0,9572976418 | 0,9572976418 |
| macro avg    | 0,8973469079 | 0,8956785072 | 0,8954465102 |
| weighted avg | 0,9568089991 | 0,9572976418 | 0,9568155579 |

# Predict

```yaml
['examination', 'of', 'the', 'data', 'from', 'all', 'ten', 'experiments', 'revealed', 'that', 'complete', 'tumor', 'tumor', 'regression', 'occurred', 'in', '14', 'of', '346', 'papilloma', 'bearing', 'mice', '4', 'that', 'were', 'treated', 'with', 'green', 'green', 'tea', 'tea', 'in', 'the', 'drinking', 'water', 'or', 'with', 'i', 'p', 'injections', 'of', 'green', 'green', 'tea', 'tea', 'constituents', 'whereas', 'none', 'of', 'the', '220', 'papilloma', 'bearing', 'control', 'mice', 'treated', 'with', 'only', 'vehicle', 'exhibited', 'complete', 'tumor', 'tumor']
['O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'disease', 'disease', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'plant', 'plant', 'plant', 'plant', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'plant', 'plant', 'plant', 'plant', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'disease', 'disease']
```

# Model Output

```yaml
-rwxrwxrwx 1 dimas dimas  617 Jun 25 20:12 config.json
-rwxrwxrwx 1 dimas dimas 414M Jun 25 20:12 pytorch_model.bin
-rwxrwxrwx 1 dimas dimas    0 Jun 27 18:31 Readme.md
-rwxrwxrwx 1 dimas dimas  112 Jun 19 13:43 special_tokens_map.json
-rwxrwxrwx 1 dimas dimas   49 Jun  1 10:14 tokenizer_config.json
-rwxrwxrwx 1 dimas dimas 209K Jun 25 20:12 vocab.txt
```