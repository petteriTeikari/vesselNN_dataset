# vesselNN_dataset

An open-source volumetric brain vasculature dataset obtained with two-photon microscopy at [Focused Ultrasound Lab](http://sunnybrook.ca/research/content/?page=sri-groups-fus), at [Sunnybrook Research Institute](http://sunnybrook.ca/research/) (affiliated with [University of Toronto]() by Dr. Alison Burgess, Charissa Poon and Marc Santos.

The dataset contains a total of 12 volumetric stacks consisting images of mouse brain vasculature and tumor vasculature.

The structure of the dataset is following:

* `denoised` contain the [BM4D](http://www.cs.tut.fi/~foi/GCF-BM3D/) denoised input stacks as multi-layer 8-bit TIFFs
* `experiments` contain the resulting images from the 1st stage of VD2D-VD2D3D recursive framework that can be fed to the VD2D3D part. Additionally both folders (`VD2D_tanh` and `VD2D3D_tanh`) that can be used as they are for inference or can be finetuned further with more data.
* `labels`contain the voxel-level dense segmentation labels for the vasculature

## Future modifications

* At the moment there is only the denoised stacks (with [BM4D](http://www.cs.tut.fi/~foi/GCF-BM3D/) which will be accompanied by the raw Poisson noise corrupted stacks straight from the Olympus FV1000MPE multiphoton microscopy system.
* At the moment in the [main repository (vesselNN)](), there are no implementations of the dataset for commonly used frameworks such as TensorFlow, Theano and Caffe which we plan to add making further development easier.
