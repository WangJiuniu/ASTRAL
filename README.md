# ASTRAL

## Paper

ASTRAL: adversarial trained LSTM-CNN for named entity recognition 
[[Link](https://www.sciencedirect.com/science/article/abs/pii/S0950705120302136), [PDF](https://arxiv.org/abs/2009.01041)]

## Dataset

We have turned the datasets' files into standard form like those in the repository [NER](https://github.com/synalp/NER/tree/master/corpus/CoNLL-2003).

CoNLL-03: resources/tasks/conll_03

OntoNotes 5.0: resources/tasks/ontoner

WNUT-17: resources/tasks/wnut_17

Here eng.train, eng.testa, and eng.testb respectively represent tran set, dev set, and test set. The files can also be downloaded from [google drive](https://drive.google.com/file/d/1lKKjVYHt2saGV5mQOuVB65xLVINyz-B5/view?usp=sharing).

## Results

**Table 1** Dataset statistics. The size of datasets is in the number of entities/tokens.

|Dataset |Train |Dev  |Test| Entities frequency |Entity  types|
|  ---  | ---- | ----- |--- |--- |--- |
|CoNLL-03 |23,499/204,567 |5,942/51,578 |5,648/46,666| 11.6% |4|
|OntoNotes 5.0 |81,828/1,088,503 |11,066/147,724 |11,257/152,728| 7.5% |18|
| WNUT-17|3,160/62,729 |1,250/15,733 |1,589/23,394| 5.9% |6|



**Table 2** Test F1 score for different models on the datasets. In this table, ‘‘∗’’ indicates the results implemented by us, and ‘‘-’’ indicates that the performances of the models on the corresponding datasets are not yet obtained.

|Model | CoNLL-03 | OntoNote 5.0 | WNUT-17|
|  ---  | ------ | ----------- |---------- |
|Character-LSTM [17]| 90.94| 84.86∗ |44.79∗|
|BLSTM-CNN [12] | 91.62 |86.28 |45.14∗|
|Stacked Multitask [18]| –| – |45.55|
|ELMo [9]|92.22 |– | –|
|CVT+Multitask [19]| 92.60| –| – |
|BERT [10]|  92.81| 88.28∗| 49.23∗|
|Contextual String Embedding [20]| 92.86 |88.75| 49.49 |
|[ASTRAL (ours)](https://arxiv.org/abs/2009.01041)| **93.32**| **89.44**| **49.72**|



## Code

To be released.

## Abstract

Named Entity Recognition (NER) is a challenging task that extracts named entities from unstructured text data, including news, articles, social comments, etc. The NER system has been studied for decades. Recently, the development of Deep Neural Networks and the progress of pre-trained word embedding have become a driving force for NER. Under such circumstances, how to make full use of the information extracted by word embedding requires more in-depth research. In this paper, we propose an Adversarial Trained LSTM-CNN (ASTRAL) system to improve the current NER method from both the model structure and the training process. In order to make use of the spatial information between adjacent words, Gated-CNN is introduced to fuse the information of adjacent words. Besides, a specific Adversarial training method is proposed to deal with the overfitting problem in NER. We add perturbation to variables in the network during the training process, making the variables more diverse, improving the generalization and robustness of the model. Our model is evaluated on three benchmarks, CoNLL-03, OntoNotes 5.0, and WNUT-17, achieving state-of-the-art results. Ablation study and case study also show that our system can converge faster and is less prone to overfitting.

## Reference

If you find this repo useful, please consider citing:

```
@article{wang2020astral,
  title={ASTRAL: adversarial trained LSTM-CNN for named entity recognition},
  author={Wang, Jiuniu and Xu, Wenjia and Fu, Xingyu and Xu, Guangluan and Wu, Yirong},
  journal={Knowledge-Based Systems},
  volume={197},
  pages={105842},
  year={2020},
  publisher={Elsevier}
}
```

## Acknowledgements

Thanks to the repository [flair](https://github.com/flairNLP/flair).