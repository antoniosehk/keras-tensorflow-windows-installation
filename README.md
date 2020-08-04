# Keras-TensorFlow-GPU-Windows-Installation (Updated: 12th Apr, 2019)
## 10 easy steps on the installation of TensorFlow-GPU and Keras in Windows

### Step 1: Install NVIDIA Driver <a href="https://www.nvidia.com/Download/index.aspx?lang=en-us" target="_blank">Download</a>
Select the appropriate version and click search
<p align="center"><img width=80% src="https://github.com/antoniosehk/keras-tensorflow-windows-installation/blob/master/NVIDIA_Driver_installation_v2.png"></p>

### Step 2: Install Anaconda (Python 3.7 version) <a href="https://www.anaconda.com/download/" target="_blank">Download</a>
<p align="center"><img width=80% src="https://github.com/antoniosehk/keras-tensorflow-windows-installation/blob/master/anaconda_windows_installation_v2.png"></p>

### Step 3: Update Anaconda
Open Anaconda Prompt to type the following command(s)
```Command Prompt
conda update conda
conda update --all
```

### Step 4: Install CUDA Tookit 10.0 <a href="https://developer.nvidia.com/cuda-downloads" target="_blank">Download</a>
Choose your version depending on your Operating System

<p align="center"><img width=90% src="https://github.com/antoniosehk/keras-tensorflow-windows-installation/blob/master/cuda10_windows10_local_installation.png"></p>

### Step 5: Download cuDNN <a href="https://developer.nvidia.com/rdp/cudnn-download" target="_blank">Download</a>
Choose your version depending on your Operating System.
Membership registration is required.

<p align="center"><img width=90% src="https://github.com/antoniosehk/keras-tensorflow-windows-installation/blob/master/cuDNN_windows_download_v2.png"></p>

Put your unzipped folder in C drive as follows: 
```Command Prompt
D:\cudnn-10.1-windows10-x64-v7.5.0.56
```
### Step 6: Add cuDNN into Environment PATH 

Add the following path in your Environment.
Subjected to changes in your installation path.
```Command Prompt
D:\cudnn-8.0-windows10-x64-v5.1\cuda\bin
```

You can either follow this <a href="https://kb.wisc.edu/cae/page.php?id=24500" target="_blank">Tutorial</a> here or the following steps (for Windows 10).

#### Step 6.1: open the Start Search, type in “env”
#### Step 6.2: choose “Edit environment variables for your account”:

<p align="center"><img width=80% src="https://github.com/antoniosehk/keras-tensorflow-windows-installation/blob/master/add_environment_variable_01.png"></p>

#### Step 6.3: under the “Users' Variables” section (the upper half), find the row with “Path” in the first column, and click edit.
<p align="center"><img width=80% src="https://github.com/antoniosehk/keras-tensorflow-windows-installation/blob/master/add_environment_variable_02.png"></p>

#### Step 6.4: the “Edit environment variable” user interface will appear. click New.

<p align="center"><img width=80% src="https://github.com/antoniosehk/keras-tensorflow-windows-installation/blob/master/add_environment_variable_03.png"></p>

Now you can add a new path to the environment varible

Turn off all the prompts. 
Open a new Anaconda Prompt to type the following command(s)
```Command Prompt
echo %PATH%
```
You shall see that the new Environment PATH is there.

### Step 7: Create an Anaconda environment with Python=3.6
Open Anaconda Prompt to type the following command(s)
```Command Prompt
conda create -n keras-gpu python=3.6 numpy scipy keras-gpu
```

### Step 8: Activate the environment
Open Anaconda Prompt to type the following command(s)
```Command Prompt
activate keras-gpu
```

### Step 9: Testing
Let's try running <a href="https://github.com/antoniosehk/keras-tensorflow-windows-installation/blob/master/examples/mnist_mlp.py">mnist_mlp.py</a> in your prompt.

Open Anaconda Prompt to type the following command(s)
```Command Prompt
activate keras-gpu
python mnist_mlp.py
```
Congratulations ! You have successfully run Keras (with Tensorflow backend) over GPU on Windows !

<p align="left"><img width=100% src="https://github.com/antoniosehk/keras-tensorflow-windows-installation/blob/master/installation_success_v2.png"></p>  

In the event that you get a tensorflow Attribute error, ensure you do the following then try again:  

`conda install -c anaconda tensorflow-estimator=2.1`

### Step 10: Done !
