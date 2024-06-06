# Cuda_10.2_installation_tutorial_on_Ubuntu_20.04/22.04
Install gcc/g++
```bash
sudo apt install build-essential
sudo apt -y install gcc-7 g++-7 gcc-8 g++-8 gcc-9 g++-9
```

Update-alternatives tool to create list of multiple GCC and G++ compiler alternatives
```bash
sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-7 7
sudo update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-7 7
sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-8 8
sudo update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-8 8
sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-9 9
sudo update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-9 9
```

Select gcc version by entering relevant selection number (select to 7)
```bash
sudo update-alternatives --config gcc
```

Select g++ version by entering relevant selection number (select to 7)
```bash
sudo update-alternatives --config g++
```

Check the gcc/g++ version
```bash
gcc --version
g++ --version
```

Download cuda 10.2
```bash
https://developer.download.nvidia.com/compute/cuda/10.2/Prod/local_installers/cuda_10.2.89_440.33.01_linux.run
```

Run cuda 10.2 installation
```bash
sudo sh cuda_10.2.89_440.33.01_linux.run
```
### Don't forget to uncheck the Cuda driver to avoid driver crashes

Set the cuda 10.2 as default
```bash
sudo apt install nano
nano ~/.bashrc
```

Add to bashrc, save and exit
```bash
export PATH=/usr/local/cuda-10.2/bin:$PATH
export LD_LIBRARY_PATH=/usr/local/cuda-10.2/extras/CUPTI/lib64:$LD_LIBRARY_PATH
export LD_LIBRARY_PATH=/usr/local/cuda-10.2/lib64:$LD_LIBRARY_PATH
```

Run the bashrc source
```bash
source ~/.bashrc
```

