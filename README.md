# AI-Powered Cyber Threat Detection Using Network Traffic Analysis

An AI/ML-based cybersecurity project that uses machine learning algorithms to classify network traffic and detect potential cyber threats across multiple network intrusion detection datasets.

## 📌 About the Project

Traditional signature-based intrusion detection systems can struggle to identify previously unseen or evolving cyber threats. This project explores the use of machine learning models to analyze network traffic and classify it into benign and malicious categories.

The project evaluates multiple machine learning algorithms across four publicly available cybersecurity datasets to study their classification performance, generalization, and ability to detect different types of attacks.

## 🎯 Objectives

- Develop a machine learning pipeline for network traffic classification and cyber threat detection.
- Compare the performance of Decision Tree, Random Forest, XGBoost, Support Vector Machine (SVM), and Logistic Regression where applicable.
- Evaluate models using accuracy, precision, recall, and F1-score.
- Investigate the effect of class imbalance and class weighting on minority attack detection.
- Use SHAP (SHapley Additive exPlanations) to help interpret model predictions.

## 📂 Project Resources

- **GitHub Repository:** [View source code and models](https://github.com/Asim0905/AI-Powered-Cyber-Threat-Detection-using-Network-Traffic-Analysis)
- **Datasets and Complete Project Materials:** [Access Google Drive Folder](https://drive.google.com/drive/folders/1-tlTSJ9Dva85eultmW4ADbdlKN3kNibV)
- **Research Paper:** [Read the Research Paper](https://drive.google.com/file/d/1MtIlH2_m1oxiKuWVQCx5jPKzvc8cCUbt/view?usp=sharing)

The GitHub repository contains the project code and models. The Google Drive folder contains the research paper, code, datasets, and other supplementary project materials. The datasets exceed 10 GB in total, so they are hosted on Google Drive rather than committed directly to GitHub.

> **Access note:** Ensure the Google Drive folder and research paper have sharing permissions suitable for your intended audience.

## 🗃️ Datasets

The project uses the following cybersecurity datasets:

1. **TON_IoT** — network and Internet of Things telemetry data for cybersecurity research.
2. **CIC-IDS2017** — network traffic data containing benign activity and multiple attack types.
3. **CICIoT2023** — a large-scale dataset for IoT attack detection.
4. **CICIoMT2024** — network traffic data for cybersecurity analysis in Internet of Medical Things environments.

Download the required dataset files from the [Google Drive folder](https://drive.google.com/drive/folders/1-tlTSJ9Dva85eultmW4ADbdlKN3kNibV), then place them in the locations expected by the relevant notebook or script. You may need to update file paths for your local environment or Google Colab.

## 🛠️ Technologies Used

- **Programming language:** Python
- **Data processing:** Pandas, NumPy
- **Machine learning:** Scikit-learn, XGBoost
- **Model explainability:** SHAP
- **Visualization:** Matplotlib, Seaborn
- **Development environment:** Jupyter Notebook / Google Colab

## 🤖 Machine Learning Models

The project evaluates the following algorithms, depending on the dataset and experiment:

- Decision Tree
- Random Forest
- XGBoost
- Support Vector Machine (SVM)
- Logistic Regression

Additional experiments investigate class weighting to improve the detection of underrepresented attack classes.

## 📊 Evaluation Metrics

| Metric | Purpose |
|---|---|
| Accuracy | Measures the proportion of correctly classified samples. |
| Precision | Measures how many predictions for a class are correct. |
| Recall | Measures how many actual samples of a class are detected. |
| Macro F1-score | Evaluates the balance between precision and recall across classes, giving each class equal weight. |
| Weighted F1-score | Calculates the F1-score while accounting for each class's support. |

Because cybersecurity datasets can be highly imbalanced, accuracy alone may not adequately represent a model's ability to detect less frequent attacks.

## 📈 Key Findings

- Tree-based models, particularly Random Forest and XGBoost, achieved strong classification performance on several evaluated datasets.
- Performance varied across datasets and attack classes, highlighting the importance of evaluating models with multiple metrics.
- In the CICIoMT2024 class-weighting experiment, macro recall increased from approximately **89.73% to 96.23%**, while accuracy decreased from approximately **99.77% to 99.17%**.
- The class-weighting experiment demonstrated that improved detection of minority classes can come at the cost of precision and overall classification performance.
- SHAP was used to help explain model predictions by estimating the contribution of input features.

These findings apply to the evaluated datasets and experimental setup; they do not establish equivalent performance on all real-world network traffic.

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/Asim0905/AI-Powered-Cyber-Threat-Detection-using-Network-Traffic-Analysis.git
cd AI-Powered-Cyber-Threat-Detection-using-Network-Traffic-Analysis
```

### 2. Set up a Python environment

Create a virtual environment:

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

Or on Linux/macOS:

```bash
source venv/bin/activate
```

### 3. Install dependencies

If the repository contains a `requirements.txt` file, install the dependencies with:

```bash
pip install -r requirements.txt
```

If it does not, install the libraries required by the notebook or script you intend to run.

### 4. Download the datasets

1. Open the [Google Drive project folder](https://drive.google.com/drive/folders/1-tlTSJ9Dva85eultmW4ADbdlKN3kNibV).
2. Download the dataset files required for your experiment.
3. Extract compressed files, if necessary.
4. Update the dataset paths in the notebook or script to match your environment.

### 5. Run the code

Open the relevant Jupyter Notebook in Jupyter Notebook or Google Colab and run its cells in order. Ensure the required dataset files and Python dependencies are available first.

## 📁 Repository Organization

The GitHub repository contains the code and model-related files. The structure below is illustrative; consult the repository for the current organization.

```text
AI-Powered-Cyber-Threat-Detection-using-Network-Traffic-Analysis/
├── models/              # Trained models or model-related files
├── notebooks/           # Notebooks, if organized in this folder
├── src/                 # Python source code, if organized in this folder
├── requirements.txt     # Python dependencies, if present
├── .gitignore
└── README.md
```

## 🔍 Explainability and Class Imbalance

The project examines class-wise performance in addition to overall accuracy. SHAP is used to help interpret feature contributions to model predictions, while class-weighting experiments investigate whether underrepresented attack classes can be detected more effectively.

## ⚠️ Limitations

- Results depend on the datasets, preprocessing steps, feature selection, and experimental configuration.
- High accuracy on benchmark datasets does not guarantee equivalent performance on unseen real-world traffic.
- Class imbalance can affect precision, recall, and F1-score differently across attack categories.
- Large datasets require sufficient storage, memory, and computational resources.
- The project should not be considered a production-ready intrusion detection system without additional testing and validation.

## 🔮 Future Improvements

- Evaluate models using a strictly independent held-out test set.
- Validate detection performance on additional unseen network traffic.
- Improve minority-class detection while controlling false positives.
- Explore real-time network traffic analysis and monitoring.
- Investigate dashboard-based monitoring and deployment as future development, where not already implemented.

## 📄 Research Paper

The research paper describing the methodology, experiments, results, and analysis is available here:

**[Read the Research Paper](https://drive.google.com/file/d/1MtIlH2_m1oxiKuWVQCx5jPKzvc8cCUbt/view?usp=sharing)**

## ⚖️ Dataset and Usage Disclaimer

The datasets originate from external research sources. Consult the respective dataset providers' terms, licenses, citation requirements, and usage restrictions before downloading, redistributing, or using the data.

This project is intended for academic research and educational purposes.
