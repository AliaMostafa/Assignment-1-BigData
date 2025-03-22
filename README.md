Basic README for Big Data Assignment 1

Project Overview

This project is a simple data processing pipeline for CSCI461 Assignment 1. It uses Docker to containerize the environment, and Python scripts to load, process, analyze, and visualize a dataset. The project also applies the K-means algorithm for clustering.

Requirements
• Docker installed on your system.
• Dataset: Place your dataset in the bd-a1/ directory (the dataset is not included in this submission).
• Docker image includes: Python3, Pandas, Numpy, Seaborn, Matplotlib, scikit-learn, and Scipy.

Project Structure
bd-a1/
├── Dockerfile
├── load.py
├── dpre.py
├── eda.py
├── vis.py
├── model.py
├── final.sh
├── service-result/     # Folder where results will be stored
└── README.md
Installation & Execution
1. Build the Docker Image:
docker build -t bd-a1-image .
2. Run the Docker Container:
docker run -it --name bd-a1-container bd-a1-image
3. Run the Pipeline Inside the Container:
python3 load.py <dataset-path>
This will execute the following steps:
• Load the dataset (load.py)
• Preprocess data (dpre.py)
• Perform exploratory data analysis (eda.py)
• Create a visualization (vis.py)
• Execute K-means clustering (model.py)

4. Retrieve Output Files:
Execute the bash script from your local machine to copy the output files from the container:
bash final.sh
Team Information
• Team Members:
Mazen Hossam 221001723
Moahmed El Morsy 221001919
Alia Moustafa 221001994
Youssef Maged 221001995
Ali Salah 221000295
