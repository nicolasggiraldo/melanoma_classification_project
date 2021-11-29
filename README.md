# Melanoma Classification Project

In this work, we show our approach to solve the [SIIM-ISIC Melanoma Classification challenge](https://www.kaggle.com/c/siim-isic-melanoma-classification). The goal of this competition is to identify melanoma from a set of skin lesion images with contextual data.


To download the dataset of the competition, run the following sentences in a bash terminal:

```
mkdir ./data
cd ./data
for input_size in 512
do
  kaggle datasets download -d cdeotte/jpeg-isic2019-${input_size}x${input_size}
  kaggle datasets download -d cdeotte/jpeg-melanoma-${input_size}x${input_size}
  unzip -q jpeg-melanoma-${input_size}x${input_size}.zip -d jpeg-melanoma-${input_size}x${input_size}
  unzip -q jpeg-isic2019-${input_size}x${input_size}.zip -d jpeg-isic2019-${input_size}x${input_size}
  rm jpeg-melanoma-${input_size}x${input_size}.zip jpeg-isic2019-${input_size}x${input_size}.zip
done
```
