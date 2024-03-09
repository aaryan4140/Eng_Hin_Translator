## English to Hindi Translation using Pretrained Model

This repository contains code for translating English text to Hindi using a pretrained model from Hugging Face. Below is an overview of the process and functionalities:

### 1. Installation and Setup
- Required libraries are installed using `pip install` commands, including `transformers`, `datasets`, `sacrebleu`, `rouge_score`, and `py7zr`.
- The `accelerate` library is upgraded and installed to enable distributed computing.

### 2. Data and Model Loading
- The pretrained model `Helsinki-nlp/opus-mt-en-hi` is used for English to Hindi translation.
- The English-Hindi translation dataset from `cfilt/iitb-english-hindi` is loaded using `datasets.load_dataset`.

### 3. Tokenization and Processing
- The `process_function` tokenizes the input English and target Hindi sentences, preparing them for the model.
- Tokenized datasets are created using `dataset.map` with the processing function.
- The `DataCollatorForSeq2Seq` class is used to combine tokens and prepare the data for the model.

### 4. Model Loading and Preparation
- The `TFAutoModelForSeq2SeqLM` loads the pretrained model for sequence-to-sequence language modeling.
- Training and validation datasets are prepared for the model using `model.prepare_tf_dataset`.

### Example Usage
- Input text, such as "I am learning coding, how about your training," is tokenized using the `tokenizer`.
- The tokenized input is prepared for the model and returned as a dictionary.

### How to Use
1. **Installation**:
   - Clone this repository and install the required libraries using the provided `pip install` commands.

2. **Data Loading**:
   - The English-Hindi translation dataset is automatically loaded from `cfilt/iitb-english-hindi`.

3. **Model Setup**:
   - The pretrained model `Helsinki-nlp/opus-mt-en-hi` is used for translation.

4. **Tokenization and Processing**:
   - Use the `process_function` to tokenize and prepare English-Hindi pairs for the model.

5. **Model Training** (Optional):
   - Train the model on the prepared datasets for English to Hindi translation.

### Note:
- This codebase is designed for translating English text to Hindi using a pretrained model.
- Users can modify input text and experiment with different sentences for translation.
- Ensure proper setup of `transformers`, `datasets`, and necessary libraries before running the code.
