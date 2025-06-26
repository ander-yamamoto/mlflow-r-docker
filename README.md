## 📦 MLflow Docker Image with R and Python

This repository provides a Docker image ready for machine learning experiment tracking using [MLflow](https://mlflow.org/) with support for both **R** and **Python 3.12**.

The image is based on either:

* `rocker/r-base` (for R-first workflows)
* `python:3.12-bookworm` (for Python-first workflows)

---

### 🔧 What's Included

* 📊 **MLflow** (installed via `pip`)
* 🐍 **Python 3.12**
* 📊 **R**
* ✅ Based on Debian Bookworm

---

### 🚀 Usage

#### Run the image:

```bash
docker run -it anderyamamoto/mlflow-r-base
```

> Replace `mlflow-r-base` with the actual image name (`mlflow-r-python` if using the Python-first version).

#### Start MLflow UI:

```bash
mlflow ui --host 0.0.0.0 --port 5000
```

Then access: [http://localhost:5000](http://localhost:5000)

---

### 📁 Example Directory Structure

```text
.
├── scripts/
│   └── train_model.R
├── README.md
```

---

### 🔪 MLflow with R Example (R script)

```r
library(mlflow)

mlflow_start_run()
mlflow_log_param("alpha", 0.01)
mlflow_log_metric("rmse", 0.75)
mlflow_end_run()
```

### 📄 License

GLP License.
See [`LICENSE`](./LICENSE) for details.
