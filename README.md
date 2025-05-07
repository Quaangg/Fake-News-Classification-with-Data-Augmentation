Cảm ơn bạn đã cung cấp liên kết tới **Kaggle Dataset**! Dưới đây là cách bạn có thể **cập nhật README** và hướng dẫn người dùng **cách tải dữ liệu từ Kaggle** sử dụng **Kaggle API**.

---

# **Fake News Classification with Data Augmentation**

## **Project Overview**

This project explores the impact of data augmentation (DA) techniques—**synonym replacement** and **function word removal**—on the performance of fake news classification models. The study leverages the **WELFake dataset** and evaluates the effectiveness of these techniques in improving model performance, focusing on models like **LSTM**, **BERT**, **GRU**, and **RNN**.

### **Datasets**

1. **Fake News Classification Dataset**:

   * **Source**: [Kaggle - Fake News Classification](https://www.kaggle.com/datasets/saurabhshahane/fake-news-classification)
   * **Description**: This dataset contains news articles along with labels indicating whether they are fake or real. The dataset can be used to train models for fake news detection.
   * **Data Columns**: Includes text data with labels for fake or real news.
   * **How to Download**:
     To download the dataset, you must use the **Kaggle API**. Follow these steps to get the dataset:

     1. **Create a Kaggle account** if you haven't already at [Kaggle](https://www.kaggle.com/).
     2. **Install Kaggle API**:
        In your terminal or command prompt, run:

        ```bash
        pip install kaggle
        ```
     3. **Get your Kaggle API key**:

        * Go to your **Kaggle account settings** [here](https://www.kaggle.com/account) and scroll to the **API** section.
        * Click on **Create New API Token**. This will download a `kaggle.json` file.
     4. **Setup the Kaggle API key**:
        Place the `kaggle.json` file in the directory `~/.kaggle/` (for Linux/macOS) or `%USERPROFILE%\.kaggle\` (for Windows).
     5. **Download the dataset**:
        Run the following command in your terminal or command prompt:

        ```bash
        kaggle datasets download -d saurabhshahane/fake-news-classification
        ```

2. **Additional Datasets**:

   * **SR Corpus**: Used for **synonym replacement** augmentation.
   * **FWD Corpus**: Used for **function word removal** augmentation.

### **Techniques Used**

1. **Synonym Replacement (SR)**:
   Replaces words in the text with synonyms from **WordNet** to increase data diversity while maintaining the original meaning. This augmentation is expected to help models generalize better.

2. **Function Word Removal (FWD)**:
   Randomly removes function words (such as “the”, “is”, etc.) based on a set probability to help the model focus on key content words that carry more meaningful information.

### **Methodology**

1. **Data Preprocessing**:

   * The **WELFake** dataset is preprocessed by converting text to lowercase, removing URLs, HTML tags, and non-alphabetical characters.

2. **Dataset Creation**:

   * **Original Dataset**: The raw dataset used for baseline comparison.
   * **Augmented Datasets**:

     * **SR Corpus**: Includes synonym replacements.
     * **FWD Corpus**: Includes function word removal.

3. **Model Training**:

   * Models such as **BERT**, **LSTM**, **GRU**, **RNN**, and **NN** are trained on the original and augmented datasets.

4. **Model Validation**:

   * The models are evaluated on a test set to assess their accuracy, precision, recall, and F1-score.

5. **Result Evaluation**:

   * The results are compared based on model performance metrics to determine which augmentation technique leads to the most improvement in classification accuracy.

### **Installation**

#### Prerequisites:

Ensure that you have **Python 3.x** installed. Then, install the required libraries using pip:

```bash
pip install pandas numpy scikit-learn nltk transformers
```

### **How It Works**

1. **Data Collection**:

   * The **Fake News Classification** dataset is downloaded using the **Kaggle API**.
   * **Synonym replacement** and **function word removal** techniques are applied to create augmented versions of the dataset.
2. **Training**:

   * Different models (**LSTM**, **BERT**, **GRU**, **RNN**) are trained on both the **original** and **augmented** datasets.
3. **Evaluation**:

   * Performance is measured by accuracy, **F1-score**, and other relevant metrics to compare the effectiveness of data augmentation techniques.

### **Main Responsibilities**

* Preprocessed the **Fake News Classification** dataset (72,134 articles) to prepare data for training.
* Implemented **synonym replacement** using **WordNet** and **function word removal** techniques to augment the dataset.
* Trained and evaluated various deep learning models (BERT, LSTM, GRU, RNN) on the augmented and original datasets.
* Analyzed **feature importance** to assess the impact of different attributes on **movie revenue**.
* Evaluated system accuracy using **user-item relevance**.

### **GitHub Repository**

* **Link to GitHub Repository**: [FakeNewsClassification](https://github.com/yourusername/FakeNewsClassification)

### **Project Duration**

6 weeks

### **Conclusion**

This research demonstrates the importance of data augmentation techniques like **synonym replacement** and **function word removal** in improving the performance of fake news classification models. By applying these techniques, the models achieved better generalization and higher classification accuracy. The results suggest that data augmentation is a promising approach to enhance model performance in complex tasks like fake news detection.
