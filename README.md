# SONAR Object Classifier
This project implements a basic classification algorithm using a perceptron model to classify objects found in a SONAR dataset, into Mines &amp; Rocks.

## Acknowledgments
Thanks to the code provided by [Matthew Carter](https://www.kaggle.com/mattcarter865). 
The code used as reference for the project is available [here](https://www.kaggle.com/mattcarter865/sonar-mines-vs-rocks/comments).

## Pseudocode of Perceptron Algorithm
1. Initialize the weights and threshold to small random numbers.
2. Present a vector X to the neuron inputs and calculate the output
3. Update the weights according to:  
    ```python
    weights[i+1] = weights[i+1] + learning_rate * error * row[i]
    ```
    where
    - `i` is the iteration number, and
    - `learning_rate` is the gain or step size, where `0.0 < n < 1.0`
4. Repeat **2 &amp; 3** until:
    - The iteration is less than a user-specified error threshold or
    - The predetermined number of iterations have been completed

## Output
*('M' denotes Mine, 'R' denotes Rock)*  
Output of the Perceptron Algorithm for the SONAR dataset with the following values
- **Folds :** 2
- **Initial Learning Rate :** 0.01
- **Epochs :** 400

The output here is taken with the same values for **folds, learning_rate and number_of_epochs** but the accuracy varies beacuse the **Cross-Validation technique** makes folds at random.
```python
{'M':0, 'R':1}

Scores : [83.65384615384616, 69.23076923076923]
Mean Accuracy : 76.442 %

Scores : [72.11538461538461, 68.26923076923077]
Mean Accuracy : 70.192 %

Scores : [70.1923076923077, 74.03846153846155]
Mean Accuracy : 72.115 %
```
