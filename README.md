# Active-Passive-Learning-using-Support-Vector-Machines
Using the banknote authentication data set, 472 data points are randomly selected as test set and remaining 900 as training. <br>
We are dealing here with a BINARY CLASSIFICATION problem. <br>
<br>
PASSIVE LEARNING : Train a SVM with a pool of 10 randomly selected data points from the training set using linear kernel and L1 penalty.
The penalty parameter is selected using 10-fold cross validation. We repeat this process by adding 10 other randomly selected data points to the pool, until all 900 points are used up. 
We have 90 SVMs that were trained using 10,20, 30, ... , 900 data points and their 90 test errors. <br>
ACTIVE LEARNING : Train a SVM with a pool of 10 randomly selected data points from the training set using linear kernel and L1 penalty.
The penalty parameter is selected using 10-fold cross validation. 
We choose the 10 closest data points in the training set to the hyperplane of the SVM4 and add them to the pool. We do not replace
the samples back into the training set. Train a new SVM using the pool.
The process is repeated until all training data is used, similarly here too we have 90 SVM's that were trained using 10, 20, 30,..., 900 data points and their 90 test errors.
<br>
Both the processes of Active and Passive Learning are repeated 50 times, into order to obtain a learning curve by MONTE-CARLO SIMULATION. 
The 50 test errors are averaged for each of the incrementally trained 90 SVM's. 
The plot of average test error versus number of training instances for both active and passive learners was made on the same figure and conclusions were reported.
