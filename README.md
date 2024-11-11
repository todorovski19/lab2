{
  "nbformat": 4,
  "nbformat_minor": 0,
  "metadata": {
    "colab": {
      "provenance": [],
      "toc_visible": true,
      "include_colab_link": true
    },
    "kernelspec": {
      "name": "python3",
      "display_name": "Python 3"
    }
  },
  "cells": [
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "view-in-github",
        "colab_type": "text"
      },
      "source": [
        "<a href=\"https://colab.research.google.com/github/jovanadobreva/Labs-I2DS/blob/main/Lab_2.ipynb\" target=\"_parent\"><img src=\"https://colab.research.google.com/assets/colab-badge.svg\" alt=\"Open In Colab\"/></a>"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "KFMjGridvepn"
      },
      "source": [
        "#<font  color='Orange'>Data Preparation & KNN Classification</font>\n"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "jaojhkPLyq8I"
      },
      "source": [
        "# <font color = 'Orange'> Read your Dataset (.csv)</font>\n",
        "run the code below for downloading the dataset"
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "!gdown 1CkUp_wtuauTNL9aOW-K52jDlTXqD4KWS"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "uwJcDAEOxf-o",
        "outputId": "4379d1ae-7291-4d8f-b1f8-2b27b74114a1"
      },
      "execution_count": 1,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "Downloading...\n",
            "From: https://drive.google.com/uc?id=1CkUp_wtuauTNL9aOW-K52jDlTXqD4KWS\n",
            "To: /content/diabetes.csv\n",
            "\r  0% 0.00/23.8k [00:00<?, ?B/s]\r100% 23.8k/23.8k [00:00<00:00, 62.5MB/s]\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "VNuwigsVwtaP"
      },
      "source": [
        "import pandas as pd\n",
        "\n",
        "df = pd.read_csv('/content/diabetes.csv')"
      ],
      "execution_count": 2,
      "outputs": []
    },
    {
      "cell_type": "code",
      "source": [
        "df.columns"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "xmpLTb2LzlQK",
        "outputId": "9c99faca-acbd-4598-d921-52e13c7ae64c"
      },
      "execution_count": 6,
      "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/plain": [
              "Index(['Pregnancies', 'Glucose', 'BloodPressure', 'SkinThickness', 'Insulin',\n",
              "       'BMI', 'DiabetesPedigreeFunction', 'Age', 'Outcome'],\n",
              "      dtype='object')"
            ]
          },
          "metadata": {},
          "execution_count": 6
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "oqwzn3eGz1rL"
      },
      "source": [
        "# <font color = 'Orange'> Data preprocessing </font>\n",
        "\n",
        "Context\n",
        "This dataset is originally from the National Institute of Diabetes and Digestive and Kidney Diseases. The objective of the dataset is to diagnostically predict whether or not a patient has diabetes, based on certain diagnostic measurements included in the dataset. Several constraints were placed on the selection of these instances from a larger database. In particular, all patients here are females at least 21 years old of Pima Indian heritage.\n",
        "\n",
        "Content\n",
        "The datasets consists of several medical predictor variables and one target variable, Outcome. Predictor variables includes the number of pregnancies the patient has had, their BMI, insulin level, age, and so on."
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "Input columns: Pregnancies, Glucose, BloodPressure,SkinThickness, Insulin, BMI, DiabetesPedigreeFunction, Age\n",
        "\n",
        "Output columns: Outcome 0-->doesn't have diabetes / 1--> has diabetes"
      ],
      "metadata": {
        "id": "Yv22PXmvzjbJ"
      }
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "WpZdCckk0Z8W"
      },
      "source": [
        "## <font color = 'Orange'>Detect the Missing values</font>"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "Gw4SkFaB1QBr"
      },
      "source": [
        "Count the percentage of missing values in every column of the Dataset."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "KI_OUR0r1XOH"
      },
      "source": [
        "#add your code"
      ],
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "ehISYUAY1qwz"
      },
      "source": [
        "#add your code"
      ],
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "bsZjZCi92J8g"
      },
      "source": [
        "## <font color = 'Orange'> Find reasons for the missing values</font>\n",
        "\n",
        "\n",
        "With the help of visualization matrix, heatmap, dendrogram, show the dependence between the columns with missing values"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "SS5AuHms1bnh"
      },
      "source": [
        "Visualize the missing values using Missingno library"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "JE-uvOiL32-v"
      },
      "source": [
        "#add your code"
      ],
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "q8TiFswE5TsD"
      },
      "source": [
        "## <font color = 'Orange'>Handle the missing values</font>"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "-gbzez457dgX"
      },
      "source": [
        "#add your code"
      ],
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "vXjNJf9v8H2Q"
      },
      "source": [
        "## <font color = 'Orange'>Save the new Dataset(.csv) without the missing values</font>"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "_cSczPJg8HGo"
      },
      "source": [
        "#add your code"
      ],
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "KSKgKX6D8Tip"
      },
      "source": [
        "Print the first rows of your final Dataset"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "fh2KI6iF8R9c"
      },
      "source": [
        "#add your code"
      ],
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "markdown",
      "source": [
        "# <font color='orange'>KNN Classification</font>"
      ],
      "metadata": {
        "id": "JQieWcUKzE8G"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "##<font color = 'Orange'>Split the dataset for training and testing in ratio 80:20 </font>\n"
      ],
      "metadata": {
        "id": "BfleC1qMWP3h"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "#add your code"
      ],
      "metadata": {
        "id": "-cfUrp-AWIGX"
      },
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "markdown",
      "source": [
        "## <font color = 'Orange'>Initialize the KNN Classification model, and use the fit function for training the model</font>"
      ],
      "metadata": {
        "id": "4K3TOKFMWfHO"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "#add your code"
      ],
      "metadata": {
        "id": "e1yWFy4mWYdl"
      },
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "markdown",
      "source": [
        "## <font color = 'Orange'>Predict the outcomes for X test</font>"
      ],
      "metadata": {
        "id": "C-9eBoB3Wh2J"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "#add your code"
      ],
      "metadata": {
        "id": "Ss1TZyPmWj0h"
      },
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "markdown",
      "source": [
        "## <font color = 'Orange'>See the model performance, by using sklearn metrics for classification</font>\n",
        "\n"
      ],
      "metadata": {
        "id": "HVgEX-dRWuPD"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "#add your code"
      ],
      "metadata": {
        "id": "afpul_fIWy1Q"
      },
      "execution_count": null,
      "outputs": []
    }
  ]
}
