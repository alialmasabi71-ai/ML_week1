\# ML Week 1 – Task 1: Environment Setup



\## 📌 Project Overview

This repository documents the complete execution of Task 1 from Week 1.

The goal was to build a clean, isolated, reproducible Machine Learning environment

and publish it to GitHub following best practices.



---



\# 🧾 Full Execution Log – Task 1



\## 1️⃣ Installed Anaconda (Windows)

\- Installed Anaconda without adding it to system PATH.

\- Avoided making Anaconda the default Python interpreter.

\- Reason: Prevent system conflicts and dependency issues.



---



\## 2️⃣ Encountered libmamba Solver Error



Error:conda-libmamba-solver (module 'libmambapy' has no attribute 'QueryFormat')



\### Resolution:

Upgraded conda and forced classic solver:conda install -n base -c conda-forge conda=25.7.0 --solver classic



Result:

Conda stabilized.



---



\## 3️⃣ Created Isolated Environment



Command: conda create -n ml\_week1 python=3.12 -y



Purpose:

\- Keep project isolated from base environment

\- Avoid dependency conflicts



---



\## 4️⃣ Activated Environment



Command: conda activate ml\_week1



Effect:

\- Switched Python interpreter

\- Switched pip

\- Isolated package installation



---



\## 5️⃣ Installed Required ML Packages



Installed:

\- numpy

\- pandas

\- scikit-learn

\- jupyterlab



Note: Used pip due to solver issues.



---



\## 6️⃣ Launched JupyterLab



Command: jupyter lab



Verified environment by running:



```python

import numpy

import pandas

import sklearn
All imports executed successfully.



##7️⃣ Exported Environment File



Command: conda env export > environment.yml


Purpose:



Capture exact dependency versions.

Enable reproducibility.





\##8️⃣ Initialized Git Repository



Commands: git init

git add environment.yml

git commit -m "Task 1: ML environment setup"





\##9️⃣ Created GitHub Repository



Repository name: ML\_week1



No README or .gitignore initially


##🔟 Linked Local Repo to GitHub

Commands: git remote add origin <repo-url>

git push -u origin main



