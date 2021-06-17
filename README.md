# ttg-parsec-migration

## parsec
cd parsec
git checkout ttg_migrate

mkdir build
mkdir build/install

cd parsec/build
../configure --prefix='path to install directory"

make install

## ttg

cd ttg
git checkout debug

mkdir build
cd build
mkdir build/install

cmake .. -DPaRSEC_ROOT_DIR="path to parsec install directory" -DCMAKE_INSTALL_PREFIX="path to ttg install directory" -DCMAKE_BUILD_TYPE=Release -DCMAKE_CXX_COMPILER=g++ -DCMAKE_C_COMPILER=gcc

make
