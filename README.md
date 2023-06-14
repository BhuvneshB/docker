# DOCKER INSTALLATION

Learnt from [**here**](https://ska-telescope.gitlab.io/sim/oskar/)



**Essential packages**

```
sudo apt-get update && 
sudo apt-get install -y build-essential  libssl-dev uuid-dev libgpgme11-dev casacore-dev cmake git libhdf5-dev python3-dev python3-pip squashfs-tools libseccomp-dev pkg-config

```
**Download, compile and install OSKAR**
```
git clone https://github.com/OxfordSKA/OSKAR.git OSKAR.git
cmake oskar -DFIND_CUDA=OFF
make -j16 
sudo make install
pip3 install 'git+https://github.com/OxfordSKA/OSKAR.git@master#egg=oskarpy&subdirectory=python'

```

**Install packages**

python3 -m pip install astropy numpy matplotlib scipy shapely h5py progressbar pyuvdata scikit-image cora python-casacore pyfiglet astroquery future pandas plotly seaborn aipy==3.0.1 aegeantools==2.2.0 
