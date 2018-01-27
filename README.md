# SUN RGBD Reorganized²

The original SUN-RGBD dataset consists of multiple small datasets that have different directory structures. As the dataset is used for RGBD semantic segmentation, it became a bit cumbersome to load images using the original `.mat` files and Ankur [re organized the dataset for semantic segmentation](https://github.com/ankurhanda/sunrgbd-meta-data).

This repository contains a bit more organized version of the Ankur's repository.

## Structure

```
./image/train/*.jpg
./image/test/*.jpg
./depth/train/*.png
./depth/test/*.png
./label13/train/*.png
./label13/test/*.png
./label37/train/*.png
./label37/test/*.png
train13.txt
test13.txt
train37.txt
test37.txt
split/test500_13.txt
split/test500_37.txt
README.md
```

In each `[train|test][13|37].txt`, I put three paths separated by a space as follows:

### train13.txt

```
image/train/img-000001.jpg depth/train/00000001.png label13/train/img13labels-000001.png
...
image/train/img-005285.jpg depth/train/00005285.png label13/train/img13labels-005285.png
```

### test13.txt

```
image/test/img-000001.jpg depth/test/00000001.png label13/test/img13labels-000001.png
...
image/test/img-005050.jpg depth/test/00005050.png label13/test/img13labels-005050.png
```

## Data Split

The main `train[13|37].txt` and `test[13|37].txt` follow the structure of [Ankur's repository](https://github.com/ankurhanda/sunrgbd-meta-data).


## Installation

```
git clone https://github.com/chrischoy/SUN_RGBD.git
cd SUN_RGBD
./download_and_extract.sh
```
