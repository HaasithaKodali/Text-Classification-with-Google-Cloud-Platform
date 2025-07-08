# 🧠 Text Classification with Google Cloud Platform (GCP)

This project presents an end-to-end **Text Classification System** built on **Google Cloud Platform (GCP)**. The goal is to categorize documents into **custom user-defined categories**, using a scalable, retrainable, and secure architecture that leverages multiple Google Cloud services such as **Cloud Storage**, **Natural Language API**, **AutoML Natural Language**, **AI Platform**, and **BigQuery**.

This system enables users to label text interactively, train TensorFlow models, evaluate and retrain them, and store categorized results in BigQuery — all via a streamlined Python-based interface.

---

## 🎯 Project Goals

- Enable custom, user-defined text classification
- Provide a simple interface for labeling and retraining models
- Use Google Cloud services for scalable, distributed model training
- Automate text analysis, category prediction, and model improvement

---

## 🧰 Technologies & Services Used

### 🔗 Google Cloud Services:
- **Cloud Storage** – Data, CSVs, and model checkpoint storage
- **Cloud Natural Language API** – Text analysis and label suggestions
- **Cloud Machine Learning Engine / AI Platform** – Model training and deployment
- **BigQuery** – Structured storage of classification results
- **Compute Engine** – Running cloud-based processing workloads
- **Identity and Access Management (IAM)** – Secure role-based access

### 🧠 ML Stack:
- **TensorFlow** – Custom model training
- **Python** – Backend orchestration, training scripts, API communication
- **AutoML Natural Language (optional)** – No-code/low-code model training
- **GCP Client Libraries** – For BigQuery, Cloud Storage, and Natural Language API

---

## 🚀 System Workflow

1. **Store Raw Text** in **Cloud Storage**
2. **Suggest Labels** via **Natural Language API**
3. **Label Training Data** via Python CLI interface
4. **Train Model** on **Cloud ML Engine** using TensorFlow
5. **Evaluate** model performance
6. **Retrain** using improved labels
7. **Store Predictions** in **BigQuery**
8. **Analyze Results** and Iterate

---

## 🛡️ Security Highlights

- **IAM Roles**: Principle of least privilege
- **KMS Encryption**: For data at rest
- **HTTPS**: For secure communication
- **IAP & VPCs**: Network isolation and identity-aware access
- **Audit Logging**: Track access and detect anomalies
- **DLP API**: Automatic redaction of sensitive information

---

## ⚙️ Scalability & Reliability

- **Distributed Training** using Cloud ML Engine (GPU-supported)
- **Auto-scaling** via Compute Engine instance templates
- **Load Balancing** for frontend/API interactions
- **Multi-region Deployment** for resilience
- **BigQuery-backed analytics** for real-time insights

---

## 🧪 Step-by-Step Execution

1. 🔧 **Create a GCP project & enable APIs**:
   - Cloud Natural Language API
   - AI Platform
   - BigQuery
   - Cloud Storage

2. 🗃️ **Prepare Data**:
   - Upload labeled text files to Cloud Storage
   - Use Python CLI to label additional data via suggested categories

3. ⚙️ **Train the Model**:
   - Use Cloud ML Engine with TensorFlow
   - Save checkpoints in Cloud Storage

4. 📈 **Classify Text & Store in BigQuery**:
   - Process articles and call `classifyText` endpoint
   - Store results with labels and confidence scores

5. 📊 **Analyze Results**:
   - Use BigQuery SQL interface for insights and analytics

---

## 📌 Sample Output

| Article Title                           | Category             | Confidence |
|----------------------------------------|-----------------------|------------|
| A Smoky Lobster Salad with a Tapa Twist | /Food & Drink         | 0.97       |
| Apple unveils new iPhone 15            | /Technology & Gadgets | 0.91       |

---

## 🚧 Challenges Addressed

- **Imbalanced datasets**: Managed using relabeling & sampling
- **Language context issues**: Enhanced via NLP suggestions
- **Model drift**: Addressed by iterative retraining
- **Security risks**: Mitigated via IAM, KMS, VPC, and monitoring

---

## 🔮 Future Directions

- 🌐 Multilingual classification
- 🧾 Industry-specific labeling pipelines
- 📷 Combine text + image classification
- 📦 GKE deployment using containers
- 📡 API gateway for public classification services

---

## 👨‍💻 Authors

- **Haasitha Kodali**  
  [Email](mailto:kodalihaasitha@gmail.com) 

- **Vardhan Reddy Jollu Bhaskar**

---

## 📜 License

This project is intended for academic and research purposes only. For commercial use, additional optimization and compliance may be required.
