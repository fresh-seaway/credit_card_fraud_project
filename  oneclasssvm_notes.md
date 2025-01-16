### One-Class SVM Hyperparameters 

| Hyperparameter | Default | Other Options | Description |
|----------------|---------|---------------|-------------|
| kernel         | `rbf`   | `linear`, `poly`, `rbf`, `sigmoid`, `precomputed` | Determines the transformation applied to the input data in a higher-dimensional space. |
| degree         | 3       | non-negative number | Only applied for the polynomial kernel to define the function's degree. |  
| gamma          | `scale` | `auto`, float | Influences the shape of the decision boundary. A smaller gamma value provides a broader decision boundary, which makes the model less sensitive to individual data points. A larger value creates a more complex decision boundary that is less sensitive to individual boundary points | 
| nu             | `0.5`   | float (0 - 1) | Provides an upper bound on the fraction of training errors and a lower bound of the fraction of support vectors. It allows users to control the balance between precision and recall in the model. A smaller nu value makes the algorithm more lenient, permitting a higher fraction of margin errors and support vectors, which can be useful in scenarios with a considerable number of anomalies. |


### Choosing a kernel function 

| Kernel    | Description |
|-----------|-------------|
| Linear Kernel (`linear`)  | Equivalent to performing a linear transformation. Suitable when the relationship between features is approximately linear. The decision boundary in the hyper-dimensional space is a hyperplane. |
| Polynomial Kernel (`poly`)    | Introduces non-linearity by considering both the dot product and higher-order interactions between features. Characterized by a user-defined degree parameter (degree). A higher degree allows the model to capture more complex relationships but may increase the risk of overfitting. |
| Radial Basis Function (`rbf`)   | Suitable for complex, non-linear relationships. Transforms data into a space where intricate decision boundaries can be draft. Useful when the exact form of relationships is unknown or intricate. |
| Sigmoid Kernel (`sigmoid`) | Suitable for scenarios where the data distribution is not well defines or exhibits sigmoidal patterns. Shape and position of the decision boundary are determined by `gamma` and `coef0`/ |