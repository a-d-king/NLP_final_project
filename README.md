# Natural Language Processing: Final Project
# By Tarun V and Adam K

Our codebase is organized as follows:
- All Jupyter notebooks besides full_pipeline.ipynb are in the directory notebooks and are used for training, data creation, fine-tuning, or any otherwise adjacent work to the creation of the end-to-end pipeline to go from a JPEG or image file through to full text expansion. The full pipeline itself is capatured by the notebook full_pipline.ipynb.
- Our project pipeline was built to run through Google Colab so to run an example start to finish you will need to reupload the existing files and directory structure.

Here is a description of this repository and its contents:

## NLP Final Project Directory Structure
  - **data/**  
    Directory containing IAM handwriting dataset and synthetic expanded data files.
    - **IAM/**
      - **image/**
        - `gpt2.dict.txt`
        - `gt_test.txt`
    - **synthetic/**
        - `df_combined_expansions.csv`
  
  - **handwriting_examples/**  
    Directory containing uploaded handwriting images.
    - `adam_writing.jpeg`
    - `tarun_writing.jpeg`
  
  - **notebooks/**  
    Directory containing Python Jupyter notebooks used in the pipeline.
    - `llama_finetuning.ipynb` - Notebook for fine-tuning our Llama model using unsloth/wandb from our synthetic data.
      - Total lines of code: 433
    - `ocr_vision_model_training.ipynb` - Notebook for training our TrOCR vision model on IAM handwriting dataset.
      - Total lines of code: 289
    - `synth_data.ipynb` - Notebook for creating synthetic data for knowledge distillation of smaller LM.
      - Total lines of code: 464
    - `vision_model_pipeline.ipynb` - Notebook for using EasyOCR to map bounding boxes in an input image file.
      - Total lines of code: 253

  - **output/**  
    Directory for storing generated text outputs.
    - `expansion_text.md` - Markdown output file with the final expanded text.

  - **full_pipeline.ipynb**   
    Jupyter notebook for the end-to-end handwriting detection and text expansion pipeline.
    - Total lines of code: 310

  - **README.md**   
    Project README file.
