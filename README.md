# treeseg

Extract individual trees from lidar point clouds

<img src="/doc/images/treeseg_cover.png" width="500">

## Description

treeseg has been developed to near-automatically extract tree-level point clouds from high-density larger-area lidar point clouds acquired in forests. A formal, albeit somewhat outdated description of the methods can be found in our paper available [here](https://doi.org/10.1111/2041-210X.13121).

## Table of contents

- [Installation](#installation)
- [Tutorial](#usage)
  - [Overview](/doc/tutorial_overview.md)
  - [Preprocessing](/doc/tutorial_preprocessing.md)
  - [Downsampling](/doc/tutorial_downsample.md)
  - [Digital terrain model](/doc/tutorial_getdemslice.md)
  - [Finding the stems](/doc/tutorial_findstems.md)
  - [Stem segmentation](/doc/tutorial_segmentstem.md)
  - [Crown segmentation](/doc/tutorial_segmentcrown.md)
- [Future work](/doc/future_work.md)
- [Acknowledgements](#acknowledgements)
- [Authors](#authors)
- [Citation](#citation)
- [License](#license)

## Installation

treeseg has been developed and tested on Ubuntu 20.04 LTS only, and has the following dependencies:

* Point Cloud Library (v1.10 or later)
* Armadillo (v9.8 or later)

These dependencies are installed via apt:

```
apt install libpcl-dev libarmadillo-dev;
```

treeseg can then be installed using:

```
git clone https://github.com/apburt/treeseg.git;
mkdir ./treeseg/build; cd ./treeseg/build; cmake ..; make;
```

Optionally, for users with RIEGL V-Line scan data, treeseg includes the executable rxp2pcd, to convert data in RXP data stream format to binary PCD format. This binary will be automatically built if the directories ./treeseg/include/reigl/ and ./treeseg/lib/riegl/ are populated with the RIEGL RiVLIB headers and libraries (as appropriate for the user's particular CPU architecture and gcc version), which can be downloaded from the Members Area of the RIEGL website (e.g., rivlib-2_5_10-x86_64-linux-gcc9.zip). 

## Usage

A tutorial demonstrating the usage of treeseg is currently under construction [here](/doc/tutorial_overview.md), which will explain the various steps required to extract the 10 largest trees from an example one hectare stand of intact old-growth tropical rainforest.

## Acknowledgements

* treeseg makes extensive use of the Point Cloud Library ([PCL](http://pointclouds.org)).

## Authors

* Andrew Burt
* Mathias Disney
* Kim Calders
* Matheus Boni Vicari
* Tony Peter

## Citation

treeseg can be cited using:

Burt, A., Disney, M., Calders, K. (2019). Extracting individual trees from lidar point clouds using *treeseg*. *Methods Ecol Evol* 10(3), 438–445. doi: 10.1111/2041-210X.13121

A doi for the latest version of treeseg is available in [releases](/releases).

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
