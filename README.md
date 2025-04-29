# Network Traffic Analysis Project

This repository contains scripts for analyzing network traffic data using various sampling techniques with PySpark and a Streamlit-based GUI. Below is a summary of the files and instructions on how to execute them.

## Dataset

The dataset used in this project is not included due to its large size. It can be downloaded from the following link:

[NetFlow Dataset - Day 2 (LANL Unified Host and Network Dataset 2017)](https://csr.lanl.gov/data-fence/1622617257/-0SFtafWP_yNOBqLkD0m8LmmTbs=/unified-host-network-dataset-2017/netflow/netflow_day-02.bz2)

Save the extracted CSV file as `input.csv` in the project directory.

---

## File Descriptions & Execution

### 📊 GUI Code

#### `proj.py`
- **Description**: Main script to launch the GUI using Streamlit.
- **Execution**:
  1. Run `streamlit run proj.py`.
  2. This will open a new tab in your default browser.
  3. Once the terminal shows the message `Ready to Recieve`, execute `input.py`.

#### `input.py`
- **Description**: Reads the `input.csv` dataset and feeds it to the processing pipeline.
- **Execution**: 
  1. Run `python input.py` to start processing the input data.

---

## ⚙️ Load Shedding Techniques

> **Note**: These scripts must be run **in parallel** with `input.py`, similar to `proj.py`.

#### `proj_uniform.py`
- **Description**: PySpark script implementing **uniform sampling**.
- **Execution**: 
  1. Run `spark-submit proj_uniform.py`.
  2. This script does not have a GUI and will output the results directly to the terminal.

#### `proj_random.py`
- **Description**: PySpark script implementing **random sampling**.
- **Execution**: 
  1. Run `spark-submit proj_random.py`.
  2. This script does not have a GUI and will output the results directly to the terminal.

---

## 🧾 Static Analysis

#### `static.py`
- **Description**: PySpark script for static data analysis.
- **Execution**: 
  1. Run `spark-submit static.py`.

---

## Notes

- Ensure that Apache Spark and Streamlit are correctly installed in your environment.
- Input data should be preprocessed and available as `input.csv` before executing the scripts.
- For accurate results, always execute `input.py` **after** the corresponding PySpark or GUI script is running.

---
