# Collaborative Memory Network for Recommendation Systems
Implementation for

Travis Ebesu, Bin Shen, Yi Fang. Collaborative Memory Network for Recommendation Systems. In Proceedings of the 41st International ACM SIGIR Conference on Research and Development in Information Retrieval, 2018.

https://arxiv.org/pdf/1804.10862.pdf


Running Collaborative Memory Network
```
python train.py --gpu 0 --dataset data/citeulike-a.npz --pretrain pretrain/citeulike-a_e50.npz
```


To pretrain the model for initialization
```
python pretrain.py --gpu 0 --dataset data/citeulike-a.npz --output pretrain/citeulike-a_e50.npz
```


**Requirements**
* Python 3.6
* TensorFlow 1.4+
* dm-sonnet


## Data Format
The structure of the data in the npz file is as follows:

```
train_data = [[user id, item id], ...]
test_data = {userid: (pos, [neg1, neg2, ...]), ...}
```

