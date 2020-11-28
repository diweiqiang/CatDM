# CatDM
[A Category-Aware Deep Model for Successive POI Recommendation on Sparse Check-in Data](https://dl.acm.org/doi/pdf/10.1145/3366423.3380202)  
Fuqiang Yu, Lizhen Cui, Wei Guo, Xudong Lu, Qingzhong Li, Hua Lu (WWW-20)

## Installation
Install tensorflow 1.12.2
The code has been tested with Python 3.5, tensorflow 1.12.2 on windows 10.

## Usage

Download datasets for training/evaluation.

### Generate Candidates

```bash
$ python train.py
```
Run 'train.py' to filter POIs and reduce the search space. Here, Encoder 1 and filtering layers form a reasonable filter capable of reducing search space, i.e., reducing the number of candidates from which recommended POIs are selected finally.

Note that the value of variable 'tf.flags.DEFINE_string' can be selected by train or test.


### Training

```bash
$ python train_rankpoi.py
```
Accurately sort the POIs in the candidate set.
