# DecompST


## Dataset Description
DecompST is quadruplet of original scene text images, text BBoxes, text-erased images, and stroke-level text mask. This dataset is made by Decomposing real-world Scene Text images into pure background images and text instances. It can be utilized to train a robust network to learn the complicated layout and the appearance of text instances in real-world scene image. 
All of the images in our dataset are collected from ICDAR2013, ICDAR-2015, and TextSeg.

<img width="700" src="./fig/samples.png">

## Download
Our dataset (TextSeg) is academia-only and cannot be used on any commercial project and research. To download the data, please send a request email to ... and tell us which school you are affiliated with.

Our dataset contains:
* ```annotation.txt``` contains original ICDAR2015-style annotation with another two labels (quality of text-stroke mask and quality of text-erased image) for each text-instance.
  * For the pixel mask image, the quality of each text instances is divided into three ranks. The text which can be clearly masked and recognized should be labeled by 1. The text which is too small to recognize or too complicated to mask should be labeled by 0. Text which are partial masked or masked imperfectly should be labeled by 3. 
  * For the text-erased image, the quality of each text instances is also divided into three ranks. The text which are perfectly erased should be labeled by 1. For the erasing result of text is bad, whose label should be 0. Text which are partially erased or the result is close to perfect should be labeled by 3.
* ```text_erased``` contains text-erased images.
* ```stroke_mask``` contains stroke-level mask of text instance. 0 means background, 255 means text.
* ```src``` contains the original images.

Text instances achieve 1 in both side will be picked up as valid data (about 16000 text instances from 4585 different images).

## Citation and Contact

Please consider to cite our paper when you use our dataset:


For any quetions about the dataset please send email to Zhengmi Tang([tzm@dc.tohoku.ac.jp]), Dr. Miyazaki([tomo@tohoku.ac.jp]) or Prof. Omachi([machi@ecei.tohoku.ac.jp]).
