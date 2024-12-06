## **AlphabetSoup Deep Learning Model Report**

###Overview
The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures.

By analyzing past application data, this model can provide insights that may guide the charity in making data-driven decisions about future funding requests. This report presents the model's structure, tuning processes, performance, and recommendations.


#### **Data Preprocessing**

- **Target Variable**:  
   - The target variable for the model was `IS_SUCCESSFUL`, which indicates whether a funding application was successful (1) or not (0).

 - **Drop Variables**:
    - Drop the non-beneficial ID columns, **EIN** and **NAME**

- **Features**:
   - The main features used for this model include **APPLICATION_TYPE** and **CLASSIFICATION** to reduce the number of categories and potentially improve model performance.
   - Convert categorical data to numeric with `pd.get_dummies`

#### **Compiling, Training, and Evaluating the Model**

- **Neural network with TensorFlow**:
When designing a neural network in TensorFlow, the choice of neurons, layers, and activation functions is crucial. Here's a breakdown of key considerations:

Start Simple: Begin with a simple architecture and gradually increase complexity.
Experimentation: Try different configurations and analyze the results.
Tried with 60, 80 and 90 in second layer and always retured the same result.

Data Complexity and Computational Resources: More complex data requires deeper and wider networks and resources, we didn't go over 100 to be more practical.


##  ** Interpreting results:**
This model achieves an accuracy of 0.7127, meaning it correctly predicts 71.27% of the test cases.
Since this is a binary classification the model is correctly classifying 71.27% of th instances


**Improving Model Performance**: We should consider the following strategies to optimize the model

Data Quality and Quantity:
- Data Cleaning: Ensure your data is clean and free of errors.
- Data Augmentation: Increase the size of your dataset by creating new data points from existing ones.
- Feature Engineering: Create new features that might be more informative.

Model Architecture:
- Experiment with Different Architectures: Try different numbers of layers, neurons, and activation functions.