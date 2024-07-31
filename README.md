# install_swan_mahameru

module purge

module load module load openmpi4/4.1.4

git clone https://gitlab.tudelft.nl/citg/wavemodels/swan.git && cd swan

mkdir build && cd build

conda install conda-forge::ninja
