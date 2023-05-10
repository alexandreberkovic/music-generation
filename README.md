# Music Generation using Diffusion Modeling

## Overview

This project aims at using diffusion models to generate spectrograms from user-defined prompts, that can then easily be converted back into sound. It uses pre-trained models from HuggingFace notably, which are further fine-tuned for our specific task. 

## Folders & Files

• data_extraction: contains notebooks enabling data extraction from Hugging Face to obtain images from MusicCaps dataset.
• description: contains the descriptions of every image, written by musicians. There are two csv files for the mono and stereo datasets.
• params_converter: contains spectogram_params.py which sets the spectrogram's parameters for the model to use, as well as other files with helper functions for im2sound and sound2im conversions and export.
• results: contains two folders; one for generated spectrogram images and one for generated music (either generated from scratch by a prompt or altered from an initial spectrogram).
• main:
  - main.ipynb: contains the main code for the text-to-image and image-to-image model pipelines.
  - stable_diff.ipynb: implementation of stable diffusion model from scratch, fine-tuned to the MusicCaps dataset.
  - sound_to_spectro.ipynb: implementations of the helper functions in params_converter to generate spectrograms from an audio file.
  - spectro_to_sound.ipynb: implementations of the helper functions in params_converter to generate sound from aspectrograms.
  

## Installation & Packages

-  Pillow 9.4.0
-  transformers 4.28.1
-  torchvision 0.15.1
-  torchaudio 2.0.1
-  torch 2.0.0
-  tokenizers 0.13.3
-  scipy 1.9.1
-  scikit-learn 1.2.2
-  scikit-image 0.20.0
-  diffusers 0.16.1

## License

MIT
