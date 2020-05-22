# Machine Learning

![](/images/ml1.png)

[Machine Learning is the] field of study that gives computers the ability to learn without being explicitly programmed. —Arthur Samuel, 1959

[Tom Mitchell (1998) Well-posed Learning Problem:] A computer program is said to learn from experience E with respect to some task T
and some performance measure P, if itsperformance on T, as measured by P, improveswith experience E. 

Repository containing a portfolio of machine learning projects and weekly progress towards becoming better at Machine Learning algorithms.

## Week 1

I have started doing Andrew Ng’s popular machine learning course on Coursera. The first week covers a lot, at least for someone who hasn’t touched much calculus for a few years.

so lets dicuss some points related to it.


## Model Representation
First, the goal of most machine learning algorithms is to construct a model: a hypothesis that can be used to estimate Y based on X. The hypothesis, or model, maps inputs to outputs. So, for example, say I train a model based on a bunch of housing data that includes the size of the house and the sale price. By training a model, I can give you an estimate on how much you can sell your house for based on it’s size. This is an example of a regression problem — given some input, we want to predict a continuous output.
The hypothesis is usually presented as:-

![](/images/LR.png)


## Cost Functions (mean difference squared)

We need a function that will minimize the parameters over our dataset. One common function that is often used is mean squared error, which measure the difference between the estimator (the dataset) and the estimated value (the prediction). It looks like this

![](/images/MSE1.png)

It turns out we can adjust the equation a little to make the calculation down the track a little more simple. We end up with:

![](/images/MSE2.png)

## Gradient Descent

We minimized J(ϴ) by trial and error above — just trying lots of values and visually inspecting the resulting graph. There must be a better way? Queue gradient descent. Gradient Descent is a general function for minimizing a function, in this case the Mean Squared Error cost function.

Gradient Descent basically just does what we were doing by hand — change the theta values, or parameters, bit by bit, until we hopefully arrived a minimum.

We start by initializing theta0 and theta1 to any two values, say 0 for both, and go from there. Formally, the algorithm is as follows:

![](/images/GD2.png)

where α, alpha, is the learning rate, or how quickly we want to move towards the minimum. If α is too large, however, we can overshoot.

![](/images/GD1.png)

## Linear Regression 

Quickly summarizing:

We have a hypothesis:

![](/images/LR.png)

which we need fit to our training data. We can use a cost function such Mean Squared Error:

![](/images/LR1.png)

which we can minimize using gradient descent:-

![](/images/LR2.png)

Which leads us to our first machine learning algorithm, linear regression. The last piece of the puzzle we need to solve to have a working linear regression model is the partial derivate of the the cost function:

![](/images/LR3.png)

Which turns out to be:-

![](/images/LR4.png)

Which gives us linear regression!

![](/images/LR5.png)

With the theory out of the way, I’ll go on to implement this logic in python.

## Week 2

