# DDAE speech enhancement

**Hyper-parameters are not tuned to optimal**

## Prerequisites:
- Keras 1.2
- Tensorflow 1.x as backend
- h5py
- librosa
- scipy

## Run (2021/07/18 RoyChao)
- `conda create --name py27 python=2.7`
- `conda activate py27`
- `pip install tensorflow=1.2`
- (maybe)`pip install keras=1.2.2`
- `pip install librosa==0.3.1`
- `pip install scikit-learn==0.16.1`
- then run commands below

## Getting Started:

Extract spectrogram features:

```sh
python spectrum.py data.h5 list_noisy list_clean
```

Train DDAE using Keras:
```sh
python train_DNN.py data.h5
```

Enhance test wave files using trained model:
```sh
python test_gen_spec.py model.hdf5 list_noisy
```
