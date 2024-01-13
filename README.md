## Installation

We need to set up our local environment to programming using python , here :

- Install and navigate through the Anaconda [Anaconda Installer](https://www.anaconda.com/download/) .

- Setup and manage the environments.

  ```conda create -n env_name```

   To access this environment through the command line : ```conda activate env_name```

   To check for the Python packages : ```conda list```

- Download Python packages in Anaconda Terminal (we can use pip or conda interchangeably).

  ```pip install pandas```

   ```pip install numpy```

   ```pip install matplotlib```

   ```pip install seaborn```

   ```pip install surprise```

    **OR**

  Install multiple packages at the same time. For example, the command below will install all three packages simultaneously.

  ```conda install pandas numpy matplotlib seaborn surprise```

- Install Jupyter Notebooks.

  ```conda install jupyter notebook```

## Coding

-  Python Integrated Development Environment (IDE) : Google Colab Notebooks.

   **Packeges used**
   
  * **pandas - numby** : used for data manipulation.
  * **matplotlib - seaborn** : used for data visualization.
  * **surprise** : used to split the dataset into train and test datasets before feeding it into the machine learning algorithm, then training the 
      dataset in ML models within this package.

## About The Dataset

- In total, this dataset has 100,004 observations and 4 features.
- Data source stored as CSV file and can be accessed through this link : [Dataset](https://raw.githubusercontent.com/hayasalman/Movie-Recommendations-System/main/ratings.csv)


