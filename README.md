# DecompST

This repository host the DecompST dataset from the following work:

**A Scene-Text Synthesis Engine via Learning from Decomposed Real-world Data** | [ArXiv](https://arxiv.org/abs/2209.02397)

Zhengmi Tang, Tomo Miyazaki, and Shinichiro Omachi.

Graduate School of Engineering, Tohoku University

You find the dataset generation code in this [Repo](https://github.com/tzm-tora/Learning-based-scene-text-engine).

## Dataset Description
DecompST is quadruplet of original scene text images, text BBoxes, text-erased images, and stroke-level text mask. This dataset is made by Decomposing real-world Scene Text images into pure background images and text instances. It can be utilized to train a robust network to learn the complicated layout and the appearance of text instances in real-world scene image. 
All of the images in our dataset are collected from ICDAR2015, ICDAR2017-MLT, and TextSeg.

<img width="700" src="./fig/samples.png">

## Download
Our dataset (DecompST) is academia-only and cannot be used on any commercial project and research. To download the data, please send a request email to us and tell us which school you are affiliated with.

Our dataset contains:
* ```annotation.txt``` contains original ICDAR2015-style annotation with another two labels (quality of text-stroke mask and quality of text-erased image) for each text-instance.
  * For the pixel mask image, the quality of each text instances is divided into three ranks. The text perfectly masked are labeled by 1. The text which is too small to recognize or too complicated to mask are labeled by 0. Text which are partial masked or near to perfect are labeled by 3. 
  * For the text-erased image, the quality of each text instances is also divided into three ranks. The text which are perfectly erased are labeled by 1. For the erasing result of text are bad, whose labels are 0. Text which are partially erased or the result is close to perfect are labeled by 3.
* ```text_erased``` contains text-erased images.
* ```stroke_mask``` contains stroke-level mask of text instances. 0 means background, 255 means text.
* ```src``` contains the original images.
* ```text_pixel``` contains text-pixel images, which can be composed by original images and stroke-level masks.

Text instances achieve 1 in both side will be picked up as valid data (about 16000 text instances from 4585 different images).

<img width="900" src="./fig/example.png">

## Citation and Contact

Please consider to cite our paper when you use our dataset:
```
@article{LBTS2022tang,
  author = {Tang, Zhengmi and Miyazaki, Tomo and Omachi, Shinichiro},
  journal = {arXiv preprint arXiv:2209.02397},
  title = {A Scene-Text Synthesis Engine Achieved Through Learning from Decomposed Real-World Data},
  year = {2022},
}
```

For any quetions about the dataset please send email to Zhengmi Tang(tzm@dc.tohoku.ac.jp), Asst Prof. Miyazaki(tomo@tohoku.ac.jp) or Prof. Omachi(machi@ecei.tohoku.ac.jp).


## Acknowledgements
Some of our data are directly from [TextSeg dataset](https://github.com/SHI-Labs/Rethinking-Text-Segmentation). Thank you for the excellent work.
