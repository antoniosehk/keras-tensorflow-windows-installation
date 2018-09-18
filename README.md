# Keras-TensorFlow-GPU-Windows-Installation
10 easy steps on the installation of TensorFlow-GPU and Keras in Windows
Note you can check for update to these instructions at the official <a href="https://www.tensorflow.org/install/install_windows">Tensorflow Installation</a> and <a href="https://keras.io/#installation">Keras Installation</a> pages.

### Step 1: Install Anaconda (Python 3.6 version) <a href="https://www.anaconda.com/download/" target="_blank">Download</a>
<p align="center"><img width=70% src="https://github.com/antoniosehk/keras-tensorflow-windows-installation/blob/master/anaconda_windows_installation.png"></p>

### Step 2: Update Anaconda
In a command window type the following command(s)
```Command Prompt
conda update conda
conda update --all
```

### Step 3: Install CUDA Tookit 9.0 <a href=" https://developer.nvidia.com/cuda-90-download-archive" target="_blank">Download</a>
Note that Tensorflow is not compatible with the most recent version of the CUDA Toolkit.  Currently you must use CUDA Toolkit 9.0.

Choose the download for your OS version.

<p align="center"><img width=70% src="https://github.com/antoniosehk/keras-tensorflow-windows-installation/blob/master/cuda8_windows7_local_installation.png"></p>

### Step 4: Download cuDNN <a href="https://developer.nvidia.com/cudnn" target="_blank">Download</a>
Be sure to choose the download for CUDA 9.0 and for your Operating System
Membership registration is required.

<p align="center"><img width=70% src="https://github.com/antoniosehk/keras-tensorflow-windows-installation/blob/master/cudnn-download.png"></p>

Put your unzipped folder in C drive as follows: 
```Command Prompt
C:\cudnn-8.0-windows10-x64-v5.1
```
### Step 5: Add cuDNN into Environment PATH <a href="https://kb.wisc.edu/cae/page.php?id=24500" target="_blank">Tutorial</a>

Add the following path in your Environment.
Subjected to changes in your installation path.
```Command Prompt
C:\cudnn-8.0-windows10-x64-v5.1\cuda\bin
```

Open a new command window and type the following command(s)
```Command Prompt
echo %PATH%
```
You should see that the new Environment PATH is there.

### Step 6: Create an Anaconda environment with Python=3.5 or Python=3.6
In the new command window, type the following command(s)
```Command Prompt
conda create -n tensorflow python=3.6 numpy scipy matplotlib spyder
```

### Step 7: Activate the environment
Type the following command(s)
```Command Prompt
activate tensorflow
```

### Step 8: Install TensorFlow-GPU
Type the following command(s)
```Command Prompt
pip install tensorflow-gpu
```

### Step 9: Install Keras
Type the following command(s)
```Command Prompt
pip install keras
```

### Step 10: Testing
Let's try running <a href="https://github.com/antoniosehk/keras-tensorflow-windows-installation/blob/master/examples/mnist_mlp.py">mnist_mlp.py</a>:

```Command Prompt
activate tensorflow
python mnist_mlp.py
```
Congratulations ! You have successfully run Keras (with Tensorflow backend) over GPU on Windows !

<p align="left"><img width=100% src="https://github.com/antoniosehk/keras-tensorflow-windows-installation/blob/master/installation_success.png"></p>
