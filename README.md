This project aims to detect spam emails using natural language processing (NLP) techniques and machine learning. The dataset contains emails labeled as spam or non-spam, and the goal is to build a model that can classify emails accurately.

## Dataset

The dataset used in this project is a CSV file containing email data with the following columns:
- `label_num`: 1 for spam, 0 for non-spam
- `text`: The content of the email

## Preprocessing

1. **Column Renaming**: The columns are renamed for better understanding.
2. **Handling Missing and Duplicate Values**: Missing values are checked, and duplicates are removed.
3. **Text Preprocessing**: The email content is preprocessed by converting to lowercase, removing non-alphanumeric characters, removing stop words, and stemming the words.

## Feature Engineering

New features are added for better analysis:
- `num_characters`: Number of characters in the email
- `num_words`: Number of words in the email
- `num_sentences`: Number of sentences in the email

## Model Training

1. **Text Vectorization**: The text is transformed using TfidfVectorizer.
2. **Train-Test Split**: The dataset is split into training and testing sets.
3. **Model Selection**: A Multinomial Naive Bayes model is trained on the training set.

## Evaluation

The model is evaluated using accuracy, confusion matrix, and classification report. A confusion matrix is also plotted for better visualization.

## Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/spam-mail-detection.git
   cd spam-mail-detection
   ```

2. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

3. Download NLTK data:
   ```python
   import nltk
   nltk.download('stopwords')
   nltk.download('punkt')
   ```

## Usage

1. Run the preprocessing and model training script:
   ```bash
   python train_model.py
   ```

## Results

The results of the model evaluation are printed in the console, including accuracy, confusion matrix, and classification report. The confusion matrix is also visualized using a heatmap.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.
