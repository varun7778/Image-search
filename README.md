# CLIP Image-Text Similarity with PyTorch

This repository demonstrates the use of OpenAI's CLIP (Contrastive Language-Image Pre-Training) model to compute image-text similarity. It compares an image with a set of predefined text labels and also allows searching for an image that best matches a query.

## Requirements

Before running the code, ensure that the following libraries are installed:

```bash
pip install transformers pillow
```

## Code Overview

1. **Loading the Model and Processor**:  
   The code uses the CLIP model and its processor from the HuggingFace Transformers library. The processor handles both image preprocessing and text tokenization.

2. **Image-Text Similarity**:  
   - The image is passed along with predefined text labels to the processor.  
   - The model then computes a similarity score between the image and each text class, and the label with the highest score is chosen as the predicted class.
   
3. **Image Search by Query**:  
   - A list of images is provided, and a textual query is given.  
   - The processor computes similarity scores between the query and each image, returning the image with the highest similarity score.

## Usage

1. **Image-Text Similarity**: The model compares an image with a set of text labels and outputs the label with the highest similarity score along with its probability.

2. **Image Search**: Given a query (e.g., "gaming console"), the model searches through a list of images and returns the one with the highest similarity score.
