Image Caption Generator | Deep Learning Project

This project focuses on generating accurate and meaningful captions for images using Deep Learning. It integrates Convolutional Neural Networks (CNNs) for extracting visual features and Long Short-Term Memory (LSTM) networks for generating descriptive captions. The model is trained using the Flickr8k dataset.

## 🚀 Project Overview

The objective of this project is to automatically describe images using natural language. This technology has several practical applications:
Assisting visually impaired individuals by describing surroundings.

*Enhancing content discovery in media libraries
*Auto-captioning images on social media and cloud storage platforms 

*Improving image search relevance

## 🧠 Model Architecture

This project utilizes an Encoder–Decoder architecture:

Component	Description
Encoder	Pre-trained CNN extracts visual features
Decoder	LSTM-based language model generates captions
Embeddings	Word embeddings created from vocabulary
Optimization	Teacher forcing + categorical crossentropy
Optional	Beam search for improved sentence generation
## 📊 Dataset — Flickr8k

8586 real-world images

40455 total text captions

Contains humans and animals in various activities

Due to size restrictions, the dataset is not included in this repository.
Place the images and captions inside a dataset/ directory after downloading.

## 📂 Folder Structure
Image-Caption-Generator/
│
├─ archive/                                          # Flickr8k images & captions (ignored in git)
├─ image-captioning-lstm-cnn.ipynb                   # Trained models, tokenizer, extracted features
├─ model.png
└─ README.md

## 🔧 Setup & Usage
1️⃣ Install Dependencies
pip install -r requirements.txt

2️⃣ Download & Place the Dataset
dataset/
 ├─ Images/
 ├─ Flickr8k.token.txt

3️⃣ Extract Image Features
python src/feature_extraction.py

4️⃣ Train the Model
python src/train.py

5️⃣ Generate Captions (Inference)
python src/inference.py --image="path_to_image.jpg"

## 📌 Sample Results
Sample Image	Model Caption
(dog image)	“a brown dog running through grass”
(child image)	“a little girl climbing up wooden steps”

You can update this section with more images from your results.

## 📈 Performance

Evaluation Metrics: BLEU Scores (insert your score here)

Performance improves with:
*Attention mechanisms
*Transformers 
*Larger datasets like Flickr30k/MS COCO

## 🛠️ Technologies Used

Python
TensorFlow / Keras
CNNs: VGG16 / InceptionV3
NLTK for caption preprocessing
NumPy, Pandas, Matplotlib for analysis

## 🚫 Dataset & File Exclusions

Large archive and dataset folders are ignored using .gitignore:
Project machine learning/Image Caption Generator/archive

## 🙌 Contribution

Contributions, ideas, and pull requests are welcome!

## 📜 License

This project is intended for educational and research purposes only.
Respect dataset usage rights as provided by the Flickr8k dataset owners.

✍️ Author

Mrityunjay Kumar
mrityunjaykumar835@gmail.com
