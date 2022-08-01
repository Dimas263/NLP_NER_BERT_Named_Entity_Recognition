# NLP
# Named Entity Recognition (NER) - BERT

## <img src="https://img.icons8.com/external-smashingstocks-flat-smashing-stocks/64/000000/external-manager-hotel-smashingstocks-flat-smashing-stocks-2.png"/> **`Slamet Riyanto S.Kom., M.M.S.I.`**

## <img src="https://img.icons8.com/external-fauzidea-flat-fauzidea/64/undefined/external-man-avatar-avatar-fauzidea-flat-fauzidea.png"/> **`Dimas Dwi Putra`**

## Architecture
<p align="center">
<img src="NER%20Architecture.png" width="7257">
</p>

## Dataset<br>[View Dataset .csv](input/)
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

## Model<br>[View BERT Model](https://huggingface.co/dmis-lab/biobert-v1.1)
```yaml
git clone https://huggingface.co/dmis-lab/biobert-v1.1
```

## Eval<br>[View Eval Report .xlsx](BERT_Report.xlsx)
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

# **Other Content**

### **Websites Prediction**
#### [1. Django Websites Prediction For NER dan RE](https://github.com/Dimas263/Django-Websites_NER_RE)


### **Named Entity Recognition (NER)**
#### [1. NER Dataset Biomedical Plant-Disease Corpus](https://github.com/Dimas263/NLP_NER_Dataset_Biomedical_Plant-Disease_Corpus)
#### [2. NER CRF Named Entity Recognition](https://github.com/Dimas263/NLP_NER_CRF_Named_Entity_Recognition)
#### [3. NER BiLSTM Named Entity Recognition](https://github.com/Dimas263/NLP_NER_BILSTM_Named_Entity_Recognition)
#### [4. NER BERT Named Entity Recognition](https://github.com/Dimas263/NLP_NER_BERT_Named_Entity_Recognition)
#### [5. NER BiLSTM CRF Named Entity Recognition](https://github.com/Dimas263/NLP_NER_BILSTM_CRF_Named_Entity_Recognition)
#### [6. NER BERT BiLSTM CRF Named Entity Recognition](https://github.com/Dimas263/NLP_NER_BERT_BILSTM_CRF_Named_Entity_Recognition)


### **Relation Extraction (RE)**
#### [1. RE Dataset Biomedical Plant-Disease Corpus](https://github.com/Dimas263/NLP_RE_Dataset_Biomedical_Plant-Disease_Corpus)
#### [2. RE BERT Relation Extraction Biomedical](https://github.com/Dimas263/NLP_RE_BERT_Relation_Extraction_Biomedical)
#### [3. RE BiLSTM CRF Relation Extraction Biomedical](https://github.com/Dimas263/NLP_RE_BILSTM_CRF_Relation_Extraction_Biomedical)
