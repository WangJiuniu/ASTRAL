# ASTRAL: adversarial trained LSTM-CNN for named entity recognition

## Abstract

Named Entity Recognition (NER) is a challenging task that extracts named entities from unstructured text data, including news, articles, social comments, etc. The NER system has been studied for decades. Recently, the development of Deep Neural Networks and the progress of pre-trained word embedding have become a driving force for NER. Under such circumstances, how to make full use of the information extracted by word embedding requires more in-depth research. In this paper, we propose an Adversarial Trained LSTM-CNN (ASTRAL) system to improve the current NER method from both the model structure and the training process. In order to make use of the spatial information between adjacent words, Gated-CNN is introduced to fuse the information of adjacent words. Besides, a specific Adversarial training method is proposed to deal with the overfitting problem in NER. We add perturbation to variables in the network during the training process, making the variables more diverse, improving the generalization and robustness of the model. Our model is evaluated on three benchmarks, CoNLL-03, OntoNotes 5.0, and WNUT-17, achieving state-of-the-art results. Ablation study and case study also show that our system can converge faster and is less prone to overfitting.

## Dataset

We have turned the datasets' files into standard form like [NER](https://github.com/synalp/NER/tree/master/corpus/CoNLL-2003).

CoNLL-03: resources/tasks/conll_03

OntoNotes 5.0: resources/tasks/ontoner

WNUT-17: resources/tasks/wnut_17

Here eng.train, eng.testa, and eng.testb respectively represent tran set, dev set, and test set. The files can also be downloaded from [google drive](https://drive.google.com/file/d/1lKKjVYHt2saGV5mQOuVB65xLVINyz-B5/view?usp=sharing).


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