# Exobrain 총괄 1세부 - 휴먼 지식증강 서비스를 위한 지능진화형 WiseQA 플랫폼 기술 개발
- 한국과학기술정보통신부 & ETRI

- 2020.09~2022.12

## Table-QA
본 저장소는 "Exobrain 총괄 1세부 - 휴먼 지식증강 서비스를 위한 지능진화형 WiseQA 플랫폼 기술 개발" 과제의 Table QA 코드 공유 및 성과를 공유하기 위한 것이다.

# Multi Paragraph Machine Reading Comprehension with Hybrid Reader over Tables and Text
This is the official repo for **Multi Paragraph Machine Reading Comprehension with Hybrid Reader over Tables and Text**, a manuscript of Heliyon.

## Abstract
In machine reading comprehension, the answer to a question could be in a table or text. Previous studies proposed combining specialized models for each table and text. Instead, we propose a Hybrid Reader Model for both the table and text with a modified K-Adapter. In the K-Adapter, the adapters are trained in a distributed manner with their weights fixed in each pre-training stage. This training process infuses table knowledge into the pre-trained model while retaining their original weights from pre-training. With a modified K-Adapter and BERT as the backbone model, our Hybrid Reader Model performs better than the specialized model on the Korean MRC dataset KorQuad 2.0.

## Model Arcitecture

#### Architecture of (a) Separated Reader Model, (b) Our Hybrid Reader Model
<center><img src="https://user-images.githubusercontent.com/64192139/212304681-038ecba6-d8d9-48b2-88fd-95075c5f0a31.png" width="70%" height="70%"></center>

#### Arcitecture of Hybrid Reader with projection
<center><img src="https://user-images.githubusercontent.com/64192139/212303898-cfa2d7b7-fba4-4300-b549-80f2f3338f40.png" width="70%" height="70%"></center>

## File Directory

```bash
├── BigBird
│   ├── MRC_bigbird.py
│   ├── MRC_Table_bigbird.py
│   └── MRC_Table_bigbird_adapter.py
├── data
│   ├── get_bigbird_dataset.py
│   └── get_ws_Data.py
├── models
│   ├── BERT_QA.py
│   ├── BERT_T_Adapter.py
│   ├── BERT_T_Adapter3.py
│   ├── BERT_T_Adapter_Stage2.py
│   ├── Dual_Encoder.py
│   └── TAPAS_with_TMN.py
├── pretrain
│   └── BERT_pretrain_adapter.py
└──  utils
    ├── attention_utils.py
    ├── Chuncker.py
    ├── DataHolder_*.py
    ├── Table_Holder.py
    ├── evalutate2.py
    ├── HTML_*.py
    ├── modeling_*.py
    ├── Ranking_ids.py
    ├── tokenization.py
    └── utils.py
``` 


## Data Preparation
KorQuAD 2.0 (https://korquad.github.io/)

## Requirements

Please install the following library requirements specified in the requirements.txt first.
If you want to download all library at once, use this code.
```bash
pip install -r requirements.txt
```

## Contrinutors
Sanghyeon Cho, Herin Kim

## License
