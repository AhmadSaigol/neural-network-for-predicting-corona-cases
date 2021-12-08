# neural-network-for-predicting-corona-cases
Predicting Corona Cases for US and for Worldwide
<br>

You can find detailed information on Dataset, Model and other parameters in the file "Report.pdf".

## Usage:

<b> Using Trained Model </b><br>
The code provides a neural network model for predicting corona cases both in US and in World. In order to use it for making predictions, follow the below procedure: 
  <ul>
    <li>Clone the repository and open the file 'NN_Prediction_Code.ipynb'in a python environment.</li>
    <li>Create a new .csv file with feature names as columns and data point as rows. You can find details on how to fill this table in 'Look_Up_Table.xlsx' (a template is also available in test folder)</li>
    <li>In the .ipynb file, run the libraries and class prediction block. Then create an object of the class by passing 'path_to_test_data.csv' and 'Optimal_thetas_of_Neural_Networks_with_metadata_*.npy' to the constructor</li>
    <li>Call the method 'prediction' on the created object and you will see the results. (a template is available in .ipynb file) </li>
  </ul>
  
  It maybe noted that the code will ignore any row with incomplete values and remove any features that were ignored during the training process. Furthermore,the code does not install any dependencies nor create any virtual environment as it was created on Google Colab.
  
  <b> Building your own Model and Training it on your own Dataset </b><br>
  
  The code allows you to build and train your own model. You can play around with the following:
  <ul>
    <li> Provide your own dataset and preprocess it</li>
    <li> Change number of layers and number of neurons</li>
    <li> Can use either Sigmoid or ReLU as activation function </li>
    <li> Can set up different hyperparameters </li>
  </ul>
  <br>
  However, you can not change other things such as:
  <ul>
    <li>The node in the output layer will always be one</li>
    <li>It will use Mean Squared Error as objective function</li>
    <li> Initialization of weights will be from uniform distribution. </li>
    <li> It will always use Gradient Descent as Optimizier</li>
    
  </ul>
  <br>
  <p> In the 'NN_Training_Code.ipynb', you would have to create an object of 'Dataset', then call 'spit_data' to create training, validation and test data and pass it in the constructor of 'Network' object along with list of number of neurons in each layer and activation function.Then you would have to call the method 'train' on its object to start the training process. Once training is done, you can simply use the same procedure (as described above) to get the predictions on the unkown dataset. </p>
  <br>
  <p>You can find more details on how to work with these layers in "Training_on_different_dataset.pdf"</p>
