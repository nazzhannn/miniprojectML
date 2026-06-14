# miniprojectML

# Intelligent Control Systems: DC Motor Behavioral Cloning

This project explores the design and implementation of an **Intelligent Behavioral Clone Controller** for a high-performance DC motor using Supervised Machine Learning. By training an Artificial Neural Network (ANN) to replicate the control policy of a classical PID controller, this project demonstrates an adaptive, data-driven approach to control systems engineering.

## 📜 Project Overview
* **Course:** MCTA 4362 Machine Learning
* **Institution:** Department of Mechatronics Engineering, IIUM
* **Objective:** Replace/Augment traditional PID loops with a data-driven Neural Network (MLPRegressor) and benchmark performance under stress.

## 🚀 Key Methodology
The project follows a "Teacher-Student" paradigm:
1. **Plant Modeling:** Discretization of continuous-time motor dynamics using Bilinear (Tustin) transformation ($\Delta t = 0.05\text{s}$).
2. **Behavioral Cloning:** Using a classical PID controller as the "Expert" to generate 600+ labeled data points (Error, Integral, Derivative $\rightarrow$ Voltage).
3. **Training:** An `MLPRegressor` (64, 32) is trained using the **Adam optimizer** and **ReLU activation** to map control inputs to optimal voltage outputs.
4. **Stress Testing:** A custom **Gradio GUI terminal** allows for real-time comparative analysis against classical PID under:
    * Ideal tracking scenarios.
    * Sensor noise injection ($\sigma=0.5$).
    * Sudden external torque disturbances (load drops).

## 🛠 Prerequisites
The project is implemented in Python. Ensure you have the following installed:
```bash
pip install numpy scipy scikit-learn matplotlib gradio

```
## 🖥 How to Run
 1. Clone this repository:
   ```bash
   git clone [YOUR-GITHUB-REPO-LINK]
   
   ```
 2. Run the main script:
   ```bash
   python Mini_project_ml_v3.ipynb
   
   ```
 3. A local URL will be generated in your terminal (e.g., http://127.0.0.1:7860). Open this in your browser to access the **Interactive Control Analysis Terminal**.
## 📊 Performance Analysis
The model was evaluated using:
 * **Mean Squared Error (MSE)**
 * **Rise Time**
 * **Overshoot (%)**
 * **Settling Time**
The results demonstrate that while the ANN effectively "clones" PID behavior under nominal conditions, it exhibits increased noise sensitivity, providing a robust discussion point for the limitations of supervised learning in non-filtered control environments.
## 🎓 Individual Contribution
As a solo project, I was responsible for:
 * **Physical Modeling:** Derivation and discretization of the DC motor system.
 * **ML Implementation:** Configuration of the MLP architecture, training pipeline, and feature engineering.
 * **Software Development:** Building the interactive Gradio GUI for real-time stress testing.
 * **Analysis:** Comparative performance benchmarking under disturbances.
## 📝 License
This project is submitted for academic assessment under the MCTA 4362 Machine Learning course at IIUM.
*Created by [Your Name] | [Date]*
```

### Pro-Tips for your GitHub Upload:
1.  **Upload your `Mini_project_ml_v3.ipynb` file:** GitHub now renders Jupyter Notebooks directly, which looks great for evaluators.
2.  **Add a `stress_test_analysis.png`:** Upload one of the graphs you generated from your Gradio GUI into the repository and link it in the `README.md` if you want to show off your results immediately!
3.  **The "Live" Demo:** Mentioning that your code *includes* an interactive GUI is a huge plus—make sure you emphasize this in the README as shown above.

```
