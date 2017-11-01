# osmcode-node

## Linux Setup
```
sudo apt-add-repository --yes ppa:chris-lea/node.js
sudo apt-add-repository --yes ppa:ubuntu-toolchain-r/test
sudo apt-get -y update
sudo apt-get -y install git gcc-4.8 g++-4.8 build-essential nodejs
sudo apt-get -y install libboost-dev zlib1g-dev libexpat1-dev libsparsehash-dev
export CC=gcc-4.8
export CXX=g++-4.8
git clone https://github.com/scrosby/OSM-binary.git
cd OSM-binary/src
make && sudo make install
```

## OSX Setup

```
git clone https://github.com/mapnik/mapnik-packaging.git
cd mapnik-packaging/osx
export CXX11=true
source MacOSX.sh
./scripts/build_bzip2.sh
./scripts/build_expat.sh
./scripts/build_google_sparsetable.sh
./scripts/build_boost.sh --with-test --with-program_options
./scripts/build_protobuf.sh
./scripts/build_osm-pbf.sh
# NOTE: in the same terminal then run the build commands
# Or from a different terminal re-run `source MacOSX.sh`
```

## Install

`npm install osmium`