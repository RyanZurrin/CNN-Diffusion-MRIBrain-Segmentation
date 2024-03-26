# Instructions for building the CNN_MASKING environment that works on modern GPUs

```bash
conda create -n tf2.10 python=3.9
conda activate tf2.10
pip install tensorflow==2.11
conda install -c anaconda cudnn
pip install nvidia-pyindex
pip install nvidia-tensorrt
conda install -c conda-forge nibabel gputil ants
pip install scikit-image>=0.16.2
pip install git+https://github.com/pnlbwh/conversion.git

```

After build the environment you need to set the LD_LIBRARY_PATH to the lib of your cuda installation:

```bash
export LD_LIBRARY_PATH=${CONDA_PREFIX}/lib/
```