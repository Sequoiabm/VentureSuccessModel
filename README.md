**Results and Overview:** 

1. **Data Preprocessing**

* **What variable(s) are the target(s) for your model?**
  Answer: The target is the Is-Successful column.
* **What variable(s) are the features for your model?**
  Features list of this model are the following: name, application type, affliation, classification, use_case, organization, income, special consideration, status, and ask amount.
* **What variable(s) should be removed from the input data because they are neither targets nor features?**
  I found two approaches. one approach involved only dropping the column "IEN" where the model yeilded 79% accuracy with 45% loss. The second approach includes dropping "EIN", "AFFILIATION", "USE_CASE" and "SPECIAL_CONSIDERATIONS". This approach yelided 80% accuracy with 50% loss. I decided the one percent increase in accuracy is not worth the loss tradeoff and will be in favor of model B instead of model C.

2. **Compiling, Training, and Evaluating the Model**

* **How many neurons, layers, and activation functions did you select for your neural network model, and why?**
  Model B: Used 4 hidden dense layers and 2 activation functions(relu and sigmoid).
  Model C: Used 4 hidden dense layers and 1 activation function (tanh).
* **Were you able to achieve the target model performance?**
  Barely. The minimum value was 75% accuracy, yet some training sessions yeilded over 97% accuracy yet output 65% accuracy in test. The goal is to have a functional model that performs exelently with minmal loss. 80% is an exelent performace and the model even achieved 84% accuracy, yet the loss for these sessions was considerably high. At the moment, 79% accuracy will have to do, but improvements iwll be made in the future.
* **What steps did you take in your attempts to increase model performance?**
  I used a combination of dropping columns, putting limits on certain data such as cutoff values in number range. The next step was altering the archatecture of the neural network by adding an extra hidden neuron layer. I found that 4 layers is the highest we can go until the model is overfit and performs worse. I also changed the activation function, finding that tanh and sigmoid result in slightly higher accuracy.

3. **Summary** :
   Overall, the accuracy for the best model was 79% accuracy and we are able to correcly classify each in the test 75% of the time. And an applicant has an 80% chance of being successful if they follow this:
   Name of applicants appears more than 5 times.
   Type of applications following T3 T4 T5 T6 T7 T8 T10 T19
   Application of the following classification ...

   **Model suggestion:**

   To potentially improve our classification results, I recommend trying a different model approach such as a Random Forest. Random Forest is a powerful ensemble learning algorithm that can handle both classification and regression tasks. It's known for its ability to handle large datasets with many features, and it can often provide better results compared to single neural network models like the ones we've used.

   Random Forest works by creating multiple decision trees and aggregating their predictions, which can reduce overfitting and improve generalization. It's a versatile algorithm and can handle both categorical and numerical data effectively. By implementing a Random Forest model, we can compare its performance with the neural network models we've tested and see if it can achieve higher accuracy and better overall results for this classification problem.

   Keep in mind that Random Forest models are less prone to overfitting compared to deep neural networks and can provide more stable and interpretable results. It's a valuable addition to our analysis toolkit.

   - By Sequoia Boubion-McKay 2024'
