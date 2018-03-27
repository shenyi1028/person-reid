# An Improved Deep Learning Architecture for Person Re-Identification

[paper link](http://www.cv-foundation.org/openaccess/content_cvpr_2015/papers/Ahmed_An_Improved_Deep_2015_CVPR_paper.pdf)

## Environment
* Ubuntu MacOS  10.13.3
* Python 3.6.4
* TensorFlow 1.4.1
* CUDA N/A
* cudnn N/A

## Installation
```
git clone https://github.com/thomaspark-pkj/person-reid.git
```

## Prepare dataset
Download CUHK03 dataset from [CUHK Person Re-identification Datasets](http://www.ee.cuhk.edu.hk/~xgwang/CUHK_identification.html) then extract file.
```
python cuhk03_dataset.py your_dataset_path
```

## Traininig
```
python run.py --data_dir=your_dataset_path
```

## Validation
```
python run.py --mode=val --data_dir=your_dataset_path
```
##### Result
Accuracy can be different slightly because image pair is generated randomly in validation dataset.
```
Accuracy: 0.846667
```

## Test
```
python run.py --mode=test --image1=your_dataset_path/labeled/val/0000_00.jpg --image2=your_dataset_path/labeled/val/0000_05.jpg
```
##### Result
```
True
```