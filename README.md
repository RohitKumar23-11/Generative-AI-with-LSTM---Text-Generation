# Generative-AI-with-LSTM---Text-Generation


```markdown
# 🧠 LSTM Text Generator

This project demonstrates how to build a **text generator using an LSTM (Long Short-Term Memory)** neural network.  
The model is trained on Shakespeare's works and can generate new, coherent text based on a given seed input.

---

## 📘 Overview

The project involves:
1. **Downloading and preprocessing** a large text dataset.
2. **Building and training** an LSTM-based neural network using TensorFlow/Keras.
3. **Generating new text** by predicting the next word in a sequence.

---

## 📂 Dataset

The dataset used in this project is **Shakespeare’s Complete Works**, available in the public domain.

You can download it manually from Project Gutenberg:  
🔗 [https://www.gutenberg.org/cache/epub/100/pg100.txt](https://www.gutenberg.org/cache/epub/100/pg100.txt)

Save the file in your project directory as:

```

shakespeare.txt

```

---

## ⚙️ Steps Performed

### 1. **Dataset Loading**
- First, I downloaded the text file from the link above.  
- Then, I loaded the data using Python and read the contents into memory.

### 2. **Text Preprocessing**
- Converted text to **lowercase**.
- Removed **punctuation** and **extra spaces** using regular expressions.
- Tokenized the text into **words** using Keras’ `Tokenizer`.

### 3. **Sequence Creation**
- Created sequences of fixed length (e.g., 30 words).
- Each sequence’s next word was used as the **target label**.

### 4. **Model Design**
- Implemented an **LSTM model** using TensorFlow/Keras:
  - Embedding Layer
  - LSTM Layer (256 units)
  - Dense Layer with Softmax Activation

### 5. **Training**
- Trained the model using **categorical crossentropy loss** and **Adam optimizer**.
- Used **early stopping** and **model checkpoints** to prevent overfitting.

### 6. **Text Generation**
- Provided a **seed sentence** (e.g., “to be or not to be”).
- The model predicted the next words iteratively to generate coherent text.

---

## 🧩 Example Seed and Output

**Seed:**  
```

to be or not to be that is the question

```

**Generated Text (example):**  
```

to be or not to be that is the question and the heart of man and the world of love and truth...

````

---

## 🧠 Experiments (Bonus)
- Tried different sequence lengths (20, 30, 40 words).
- Tested deeper LSTM architectures.
- Tuned the temperature parameter for more or less creative text.

---

## 🛠️ Requirements

- Python 3.x  
- TensorFlow / Keras  
- NumPy  
- Requests  
- scikit-learn  

Install dependencies with:

```bash
pip install tensorflow numpy requests scikit-learn
````

---

## 🏁 How to Run

1. Download the dataset manually:

   ```
   https://www.gutenberg.org/cache/epub/100/pg100.txt
   ```
2. Save it as:

   ```
   shakespeare.txt
   ```
3. Run the script:

   ```bash
   python lstm_text_generator.ipynb
   ```
4. Wait for training to complete, and view the generated text outputs.

---

## 📄 License

This project uses text from **Project Gutenberg**, which is in the **public domain**.
You may use and modify this code freely for educational and research purposes.

---

**Author:** Rohit Kumar
**Model Type:** LSTM-based Text Generator
**Dataset Source:** Project Gutenberg (Shakespeare’s Complete Works)

```
