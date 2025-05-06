# **Unit 9 Exercises: Matrix Multiplication is all you need?**

We won't just talk about matrix multiplication in these exercises: we'll also play with a neuarl network visualization in order to get some intuition on how to properly parameratize neural networks.

**Task1**:

Play with the web app at this [link](http://matrixmultiplication.xyz/).

Explain what happens when we do matrix multiplication.

Yes, I know I basically already asked you to do this in the notes. Don't copy and paste your answer from before; honestly do the exercise again.

Each row of numbers in the first matrix is multiplied by the column of numbers in the second matrix. The result of each multiplication is summed and added to the first available spot in the next matrix. This multiplication happens until all rows have been multiplied by both columns, and a full new matrix is made.

**Task2**:

Look at code for any neural network, such as my notes, or any other source.

1. Point out where in the code the neural network is multiplying matricies.  
2. Conceptually, what part of a neural network is that matrix multiplication that you pointed out? In other words, what does matrix multiplication do for a neural network?

→ y\_pred \= linear(X) \#the actual matrix multiplication

That matrix multiplication is used to make the OLS, and then the estimand. 

**Task3**:

Go to the [TensorFlow Playground website](https://playground.tensorflow.org/#activation=tanh&batchSize=10&dataset=circle&regDataset=reg-plane&learningRate=0.03&regularizationRate=0&noise=0&networkShape=4,2&seed=0.16540&showTestData=false&discretize=false&percTrainData=50&x=true&y=true&xTimesY=false&xSquared=false&ySquared=false&cosX=false&sinX=false&cosY=false&sinY=false&collectStats=false&problem=classification&initZero=false&hideText=false).

Explain what part of the neural network visualization is matrix multiplication.

Layer 1 is raw inputs (matrixes of raw data). Hidden layer generates the hidden weights. The matrix multiplication occurs on the line that connects the initial nodes to the next ones. 

**Task4**:

Go to the [TensorFlow Playground website](https://playground.tensorflow.org/#activation=tanh&batchSize=10&dataset=circle&regDataset=reg-plane&learningRate=0.03&regularizationRate=0&noise=0&networkShape=4,2&seed=0.16540&showTestData=false&discretize=false&percTrainData=50&x=true&y=true&xTimesY=false&xSquared=false&ySquared=false&cosX=false&sinX=false&cosY=false&sinY=false&collectStats=false&problem=classification&initZero=false&hideText=false).

Set up the scenario with the following characteristics:

* problem type: regression  
* Data: multi guassian  
* Ratio: 80% training  
* Noise: 20  
* Batch size: 15  
* Discretize output: start with it checked on

You may turn discretize output on or off once you get an idea of what to do, so you can see what each node is doing.

Goal: get your test loss to under **0.03**.

You may change any of the other parameters that I didn't explicitly tell you to set up. Remember to use the back/restart button inbetween model adjustments.

Your answer will be a link to the model you created. How do you get that link? Once you've achieved the appropriate test loss, copy and paste the url.

[https://playground.tensorflow.org/\#activation=tanh\&batchSize=15\&dataset=circle\&regDataset=reg-gauss\&learningRate=0.03\&regularizationRate=0\&noise=20\&networkShape=4,2,3\&seed=0.89345\&showTestData=false\&discretize=false\&percTrainData=80\&x=true\&y=true\&xTimesY=true\&xSquared=false\&ySquared=false\&cosX=false\&sinX=true\&cosY=false\&sinY=false\&collectStats=false\&problem=regression\&initZero=false\&hideText=false](https://playground.tensorflow.org/#activation=tanh&batchSize=15&dataset=circle&regDataset=reg-gauss&learningRate=0.03&regularizationRate=0&noise=20&networkShape=4,2,3&seed=0.89345&showTestData=false&discretize=false&percTrainData=80&x=true&y=true&xTimesY=true&xSquared=false&ySquared=false&cosX=false&sinX=true&cosY=false&sinY=false&collectStats=false&problem=regression&initZero=false&hideText=false)

**Task5**:

Go to the [TensorFlow Playground website](https://playground.tensorflow.org/#activation=tanh&batchSize=10&dataset=circle&regDataset=reg-plane&learningRate=0.03&regularizationRate=0&noise=0&networkShape=4,2&seed=0.16540&showTestData=false&discretize=false&percTrainData=50&x=true&y=true&xTimesY=false&xSquared=false&ySquared=false&cosX=false&sinX=false&cosY=false&sinY=false&collectStats=false&problem=classification&initZero=false&hideText=false).

Set up the scenario with the following characteristics:

* problem type: classification  
* Data: circle  
* Ratio: 80% training  
* Noise: 0  
* Batch size: 15

Goal: get your test loss to under **0.005**.

You may change any of the other parameters that I didn't explicitly tell you to set up. Remember to use the back/restart button inbetween model adjustments.

Your answer will be a link to the model you created. How do you get that link? Once you've achieved the appropriate test loss, copy and paste the url.

[https://playground.tensorflow.org/\#activation=tanh\&batchSize=15\&dataset=circle\&regDataset=reg-gauss\&learningRate=0.03\&regularizationRate=0\&noise=0\&networkShape=4,3,4\&seed=0.22847\&showTestData=false\&discretize=false\&percTrainData=80\&x=true\&y=true\&xTimesY=true\&xSquared=false\&ySquared=false\&cosX=false\&sinX=true\&cosY=false\&sinY=false\&collectStats=false\&problem=classification\&initZero=false\&hideText=false](https://playground.tensorflow.org/#activation=tanh&batchSize=15&dataset=circle&regDataset=reg-gauss&learningRate=0.03&regularizationRate=0&noise=0&networkShape=4,3,4&seed=0.22847&showTestData=false&discretize=false&percTrainData=80&x=true&y=true&xTimesY=true&xSquared=false&ySquared=false&cosX=false&sinX=true&cosY=false&sinY=false&collectStats=false&problem=classification&initZero=false&hideText=false) 

**Task6**:

Go to the [TensorFlow Playground website](https://playground.tensorflow.org/#activation=tanh&batchSize=10&dataset=circle&regDataset=reg-plane&learningRate=0.03&regularizationRate=0&noise=0&networkShape=4,2&seed=0.16540&showTestData=false&discretize=false&percTrainData=50&x=true&y=true&xTimesY=false&xSquared=false&ySquared=false&cosX=false&sinX=false&cosY=false&sinY=false&collectStats=false&problem=classification&initZero=false&hideText=false).

Set up the scenario with the following characteristics:

* problem type: classification  
* Data: spiral  
* Ratio: 80% training  
* Noise: 20  
* Batch size: 15

Goal: get your test loss to under **0.05**.

You may change any of the other parameters that I didn't explicitly tell you to set up. Remember to use the back/restart button inbetween model adjustments.

Your answer will be a link to the model you created. How do you get that link? Once you've achieved the appropriate test loss, copy and paste the url.

[https://playground.tensorflow.org/\#activation=tanh\&regularization=L1\&batchSize=15\&dataset=spiral\&regDataset=reg-gauss\&learningRate=0.3\&regularizationRate=0\&noise=20\&networkShape=5,3\&seed=0.26636\&showTestData=false\&discretize=false\&percTrainData=80\&x=true\&y=true\&xTimesY=true\&xSquared=false\&ySquared=false\&cosX=false\&sinX=true\&cosY=false\&sinY=true\&collectStats=false\&problem=classification\&initZero=false\&hideText=false](https://playground.tensorflow.org/#activation=tanh&regularization=L1&batchSize=15&dataset=spiral&regDataset=reg-gauss&learningRate=0.3&regularizationRate=0&noise=20&networkShape=5,3&seed=0.26636&showTestData=false&discretize=false&percTrainData=80&x=true&y=true&xTimesY=true&xSquared=false&ySquared=false&cosX=false&sinX=true&cosY=false&sinY=true&collectStats=false&problem=classification&initZero=false&hideText=false) 