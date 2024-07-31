# install_swan_mahameru

module purge

module load gnu/12.2.0

module load gcc/12.2.0

module load openmpi/4.1.1

module load cmake/3.24.2

git clone https://gitlab.tudelft.nl/citg/wavemodels/swan.git && cd swan

mkdir build && cd build

conda install conda-forge::ninja
