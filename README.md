# Bayesian Skip Net

Perfusion CT is widely used in acute ischemic stroke to determine eligibility for acute treatment, by defining an ischemic core and penumbra. In this work presented at the Brain Lesion Workshop at MICCAI 2020, we used a novel way of building on prior information for the automatic prediction and segmentation of stroke lesions. We reformulate the task to identify differences from a prior segmentation by extending a three-dimensional Attention Gated Unet with a skip connection allowing only an unchanged prior to bypass most of the network. We show that this technique improves results obtained by a baseline Attention Gated Unet on both the Geneva Stroke Dataset and the ISLES 2018 dataset.

Please cite as: Klug, J. et al. Bayesian Skip Net: Building on Prior Information for the Prediction and Segmentation of Stroke Lesions. in Brainlesion: Glioma, Multiple Sclerosis, Stroke and Traumatic Brain Injuries (eds. Crimi, A. & Bakas, S.) 168–180 (Springer International Publishing, 2021). doi:10.1007/978-3-030-72084-1_16.


## Video explanation

Click on the image below:

[![Bayesian Skip Net Presentation](https://img.youtube.com/vi/PbyxpUMV8-w/0.jpg)](https://www.youtube.com/watch?v=PbyxpUMV8-w)

## Model Architecture

![Bayesian Skip Net Architecture](/static/figures/bayesian_skip_net/bayesian_skip_net.svg)

## Installation
`pip install -r requirements.txt`

##### Compatibility

- Environment must use python 3.7 (for torch and CUDA compatibility)

## Getting started

- The main file for training can be found under `train_segmentation.py`. It takes a config file as argument, examples can be found in the `./config`folder. 
- A visdom server can be launched as well for visualisation: `python -m visdom.server`

## References

- "Attention U-Net: Learning Where to Look for the Pancreas", MIDL'18, Amsterdam, [original paper](https://openreview.net/pdf?id=Skft7cijM) <br />
- Clinical implications: https://jamanetwork.com/journals/jamanetworkopen/fullarticle/2762679

## This is a stale repo

- Active development repo: https://github.com/JulianKlug/PerfusionCT-Net
