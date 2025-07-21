# 📊 News Article Classification – ML Project Lifecycle

**Transform raw headlines into actionable insights** with a production-ready news classifier that’s **fast**, **accurate**, and **scalable**.

---

## 🔍 **Project Overview**

A one-stop solution for **automated news filtering** in aggregation apps:

* Follows the **full ML lifecycle**—from data exploration to model deployment
* Targets **multi-topic classification** using only article titles
* Deployed via **TensorFlow Serving** for **real-time predictions**

---

## ⚡ **Key Features**

* **Robust Preprocessing**: Tokenization, embedding (10k vocab, 24-dim), padded sequences (max length = 20)
* **Balanced Experiments**: Baseline model (78% accuracy) vs. class-imbalance strategies
* **Modular Architecture**:

  * `lab_utils.py` for directory management & data loading
  * `e1/` and `e2/` folders for isolated experiment runs
* **Production-Ready Serving**:

  * **Docker-friendly** TF-Serving commands
  * Built-in support for **A/B testing** and **versioning**

---

## 🛠️ **Installation & Setup**

1. **Clone** this repo:

   ```bash
   git clone https://github.com/sohailshk/News_Filtering_InProduction && cd news-classifier
   ```
2. **Create** a virtual environment & install dependencies:

   ```bash
   python3 -m venv venv && source venv/bin/activate
   pip install -r requirements.txt
   ```
3. **Launch** Jupyter & explore:

   ```bash
   jupyter notebook News_Filtering__Orignal.ipynb
   ```

---

## ▶️ **Usage**

1. **Train** the model: follow 🔢 Preprocessing → 📊 Training → 📉 Evaluation in the notebook
2. **Serve** your best model:

   ```bash
   tensorflow_model_server \
     --rest_api_port=8501 \
     --model_name=news_classifier \
     --model_base_path=./e2/model/
   ```
3. **Predict** via `curl` or client call to `/v1/models/news_classifier:predict`

---

> **Why choose this solution?**
>
> 1. **Speed**: Lightweight architecture for sub-second inference
> 2. **Accuracy**: Proven 78%+ baseline, easily extendable
> 3. **Scalability**: Containerized TF-Serving for seamless integration

---

## 📞 **Get in Touch**

For **partnership**, **customization**, or **support**, contact **[your.name@example.com](mailto:your.name@example.com)**.
Let’s **revolutionize** how the world consumes news—**today!**
