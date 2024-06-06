# Cuda_10.2_installation_tutorial_on_Ubuntu_20.04/22.04
install gcc/g++
```bash
sudo apt install build-essential
sudo apt -y install gcc-7 g++-7 gcc-8 g++-8 gcc-9 g++-9
```

update-alternatives tool to create list of multiple GCC and G++ compiler alternatives
```bash
sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-7 7
sudo update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-7 7
sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-8 8
sudo update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-8 8
sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-9 9
sudo update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-9 9
```

select GCC version by entering relevant selection number (select to 7)
```bash
sudo update-alternatives --config gcc
```

select G++ version by entering relevant selection number (select to 7)
```bash
sudo update-alternatives --config g++
```

check the GCC/G++ version
```bash
gcc --version
g++ --version
```

Download cuda 10.2
```bash
https://developer.download.nvidia.com/compute/cuda/10.2/Prod/local_installers/cuda_10.2.89_440.33.01_linux.run
```

run cuda 10.2 installation
```bash
sudo sh cuda_10.2.89_440.33.01_linux.run
```
### Don't forget to uncheck the Cuda driver to avoid driver crashes
