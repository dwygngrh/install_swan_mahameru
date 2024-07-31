# install_swan_mahameru

module purge

module load openmpi4/4.1.4

module load cmake/3.24.2

conda deactivate

# Bisa ditaro di .bashrc tapi harus hati hati

export mpignu=/opt/ohpc/pub/mpi/openmpi4-gnu12/4.1.4

export LD_LIBRARY_PATH=${mpignu}/lib:$LD_LIBRARY_PATH

export PATH=${mpignu}/include:$PATH

# download swan

git clone https://gitlab.tudelft.nl/citg/wavemodels/swan.git && cd swan

mkdir build && cd build

cmake .. -G "Unix Makefiles"

make

cmake --install . --prefix /mgpfs/home/dwiy008/swan/install   # ganti dwiy008 dengan username pak agus dendy

# instalasi selesai


