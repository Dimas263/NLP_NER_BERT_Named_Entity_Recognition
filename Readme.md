# NLP
# Named Entity Recognition (NER) - BERT

## <img src="https://img.icons8.com/external-smashingstocks-flat-smashing-stocks/64/000000/external-manager-hotel-smashingstocks-flat-smashing-stocks-2.png"/> **`Slamet Riyanto S.Kom., M.M.S.I.`**
4
​
5
## <img src="https://img.icons8.com/external-fauzidea-flat-fauzidea/64/undefined/external-man-avatar-avatar-fauzidea-flat-fauzidea.png"/> **`Dimas Dwi Putra`**

## Architecture
<img src="NER%20Architecture.png" width="7257">

## Dataset
| Sentence #  | Word        | POS | Tag       |
| ----------- | ----------- | --- | --------- |
| Sentence: 0 | studies     | NNS | O         |
| Sentence: 0 | on          | IN  | O         |
| Sentence: 0 | magnesium   | NN  | O         |
| Sentence: 0 | s           | NN  | O         |
| Sentence: 0 | mechanism   | NN  | O         |
| Sentence: 0 | of          | IN  | O         |
| Sentence: 0 | action      | NN  | O         |
| Sentence: 0 | in          | IN  | O         |
| Sentence: 0 | digitalis   | NN  | B-plant   |
| Sentence: 0 | induced     | VBD | O         |
| Sentence: 0 | arrhythmias | NNS | B-disease |
...

## Model 
```yaml
git clone https://huggingface.co/dmis-lab/biobert-v1.1
```

## Eval
| Entities     | precision | recall | f1-score | support | Train Batch Size | Valid Batch Size | Epochs | Learning Rate | Max Grad Norm | execution time |
| ------------ | --------- | ------ | -------- | ------- | ---------------- | ---------------- | ------ | ------------- | ------------- | -------------- |
| O            | 96,03%    | 96,77% | 96,40%   | 4645    | 8                | 4                | 25     | 0,00001       | 10            | 0.20.11        |
| disease      | 72,49%    | 64,38% | 68,19%   | 393     |                  |                  |        |               |               |                |
| plant        | 81,31%    | 83,63% | 82,46%   | 281     |                  |                  |        |               |               |                |
| accuracy     | 93,68%    | 93,68% | 93,68%   | 0       |                  |                  |        |               |               |                |
| macro avg    | 83,28%    | 81,59% | 82,35%   | 5319    |                  |                  |        |               |               |                |
| weighted avg | 93,51%    | 93,68% | 93,58%   | 5319    |                  |                  |        |               |               |                |
| F-1 Scores   |           |        | 93,68%   |         |                  |                  |        |               |               |                |

## Predict
```yaml
['examination', 'of', 'the', 'data', 'from', 'all', 'ten', 'experiments', 'revealed', 'that', 'complete', 'tumor', 'tumor', 'regression', 'occurred', 'in', '14', 'of', '346', 'papilloma', 'bearing', 'mice', '4', 'that', 'were', 'treated', 'with', 'green', 'green', 'tea', 'tea', 'in', 'the', 'drinking', 'water', 'or', 'with', 'i', 'p', 'injections', 'of', 'green', 'green', 'tea', 'tea', 'constituents', 'whereas', 'none', 'of', 'the', '220', 'papilloma', 'bearing', 'control', 'mice', 'treated', 'with', 'only', 'vehicle', 'exhibited', 'complete', 'tumor', 'tumor']
['O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'disease', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'plant', 'plant', 'plant', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'plant', 'plant', 'plant', 'plant', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'disease', 'disease']
```
## Output
## New Pretrained Model [BioBert-Plant-Disease](output/biobert-plant-disease) 