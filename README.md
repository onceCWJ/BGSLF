# Balanced Spatial-Temporal Graph Structure Learning for Multivariate Time Series Forecasting: A Trade-off between Efficiency and Flexibility
## Accepted by ACML2022
## Requirements
- Python 3.8.3
- see `requirements.txt`

## Data Preparation

#### H5 File
Download the traffic data files for Los Angeles (METR-LA) from [Google Drive](https://drive.google.com/open?id=10FOTa6HXPqX8Pf5WRoRwcFnW9BrNZEIX) or [Baidu Yun](https://pan.baidu.com/s/14Yy9isAIZYdU__OYEQGa_g) links provided by [DCRNN](https://github.com/liyaguang/DCRNN). Put into the `data/{METR-LA,PEMS-BAY}` folder.

#### TXT File
Download Solar-Energy datasets from [https://github.com/laiguokun/multivariate-time-series-data](https://github.com/laiguokun/multivariate-time-series-data). Put into the `data/{solar_AL}` folder.

#### NPZ File

Download PEMS04, PEMS08 datasets from [https://github.com/Davidham3/ASTGCN/tree/master/data). Put into the `data/{PEMS04,PEMS08}` folder.

## Split dataset

Run the following commands to generate train/validation/test dataset at `data/{METR-LA,PEMS-BAY,solar_AL,traffic,electricity,exchange_rate,PEMS04,PEMS08}/{train,val,test}.npz`.

```
python generate_data.py --dataset METR-LA

python generate_data.py --dataset PEMS04

python generate_data.py --dataset PEMS08

python generate_data.py --dataset Solar_AL
```

## Train Commands

* METR-LA
```
# Use METR-LA dataset
python train.py --dataset_dir=data/METR-LA
```

* Solar-Energy
```
# Use Solar-Energy dataset
python train.py --dataset_dir=data/solar_AL
```
* PEMS04
```
# Use PEMS04 dataset
python train.py --dataset_dir=data/PEMS04
```
* PEMS08
```
# Use PEMS08 dataset
python train.py --dataset_dir=data/PEMS08
```


# Citation Format
If you find this codebase helpful for your research, please consider citing the following paper:

```plaintext
@inproceedings{chen2023balanced,
  title={Balanced spatial-temporal graph structure learning for multivariate time series forecasting: a trade-off between efficiency and flexibility},
  author={Chen, Weijun and Wang, Yanze and Du, Chengshuo and Jia, Zhenglong and Liu, Feng and Chen, Ran},
  booktitle={Asian Conference on Machine Learning},
  pages={185--200},
  year={2023},
  organization={PMLR}
}
```
This version of implementation is only for learning purposes. For research, please refer to the following url:
https://proceedings.mlr.press/v189/chen23a.html
