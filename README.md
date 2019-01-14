# gradient_descent-tf

**Gradient descent algorithm** implementation using **tensorflow.js**.

## Description:

Gradient descent is an optimization algorithm used to find the values of parameters (coefficients) of a function (f) that minimizes a cost function (cost).

## Project goal and data set:

In this project, the goal is to **predict** the **fuel efficiency of a car**.
3 features of the data set are used for the predictions:

- **horsepower** (unit of measurement of power).
- **weight** (amount of a car weight).
- **displacement** (swept volume of pistons inside the cylinders).

The data set can be found in **cars.csv** file.

## Structure of linear-regression.js file:

```
class LinearRegression {
    gradientDescent()     // Run one iteration of Gradient Descent and update "m and "b.
    train()               // Run Gradient Descent until good values for "m" and "b are found.
    test()                // Use a "test" data set to evaluate the accuracy of the calculated "m" and "b".
    predict()             // Make a prediction using the calculated "m" and "b".
}
```

## Batch Gradient Descent:
- Guess a starting value of B, M and learning rate
- Standerize data
- Calculate Slope of Mean Squared Error (MSE)  using a portion of observations in feaure set and current M/B values
- Multiply the slope by the learning rate
- Update B and M
- Calculate the Coeficient of Determination
- Record MSE history and optimize/adjust the learning rate 
- Adjust iterations number and  batch size
- Evaluate result
- Make predictions

## Result and predictions:
Coefcient of determiantion = 0.668

| Horsepower | Weight | Displacement | Result in MPG |
| --- | --- | --- | --- |
| 120 | 2 | 380 | 16.16 |
| 150 | 2.3 | 430 | 11.58 |

## How to run analysis:

- Clone repository
- Install node packages (npm install)
- In the terminal under gradient_descent-tf directory run: node index.js
