# Home Credit Risk Analysis

<h1>Overview </h1>
The objective of the Home Credit Default Risk project is to assess a client's ability to repay a loan based on a collection of features present in the dataset.
In phase 1, we identified the problem as a classification task and selected suitable ML models. Phase 2 involved EDA and creating baseline models with four different algorithms. In Phase 3, we conducted additional feature engineering to identify the most effective features and used GridSearch to refine the accuracy of our models further. We observed that the XGBoost produced a Kaggle score of 0.736.
During the final phase, our aim was to implement Multilayer Perceptron architectures to analyze our data and evaluate the performance based on the binary cross-entropy loss function. We utilized the ReLU activation function for the hidden layer and sigmoid for the output layer with the Adam optimizer and performed 50 epochs using 3 hidden layers and 1 output feature. Additionally, we utilized TensorBoard to visualize our accuracy and loss. As a result, we achieved a test ROC of 0.76, with a Kaggle submission public score of 0.728.

<h1>Data files overview</h1>

<p>There are 7 different sources of data:</p>

<ul>
  <li>application_train/application_test (307k rows, and 48k rows): the main training and testing data with information about each loan application at Home Credit. Every loan has its own row and is identified by the feature SK_ID_CURR. The training application data comes with the TARGET indicating 0: the loan was repaid or 1: the loan was not repaid. The target variable defines if the client had payment difficulties meaning he/she had late payment more than X days on at least one of the first Y installments of the loan. Such case is marked as 1 while other all other cases as 0.</li>
</ul>

<ul>
  <li>bureau (1.7 Million rows): Data concerning client's previous credits from other financial institutions. Each previous credit has its own row in bureau, but one loan in the application data can have multiple previous credits.</li>
</ul>


<ul>
  <li>bureau_balance (27 Million rows) :Monthly data about the previous credits in bureau. Each row is one month of a previous credit, and a single previous credit can have multiple rows, one for each month of the credit length.</li>
</ul>


<ul>
  <li>previous_application (1.6 Million rows) : Previous applications for loans at Home Credit of clients who have loans in the application data. Each current loan in the application data can have multiple previous loans. Each previous application has one row and is identified by the feature SK_ID_PREV.</li>
</ul>


<ul>
  <li>POS_CASH_BALANCE (10 Million rows): Monthly data about previous point of sale or cash loans clients have had with Home Credit. Each row is one month of a previous point of sale or cash loan, and a single previous loan can have many rows.</li>
</ul>

<ul>
  <li>credit_card_balance: Monthly data about previous credit cards clients have had with Home Credit. Each row is one month of a credit card balance, and a single credit card can have many rows.</li>
</ul>

<ul>
  <li>installments_payment (13.6 Million rows): Payment history for previous loans at Home Credit. There is one row for every made payment and one row for every missed payment.</li>
</ul>
<img width="496" alt="Screenshot 2023-06-19 at 11 36 58 AM" src="https://github.com/aaru9dua/Machine-learning/assets/46483403/b62adb58-12b4-44b2-bc8e-1263dbe3a13b">

