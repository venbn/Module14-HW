# Machine Learning Trading Bot

![Decorative image.](Images/14-challenge-image.png)

Now, it's time to take what you've learned about machine learning and apply it to new situations. For this optional assignment, you'll create an algorithmic trading bot that learns and adapts to new data and evolving markets. Be sure to give it your all -- as the skills you hone will become powerful tools in your FinTech tool belt.

## Background

In this Challenge, you’ll assume the role of a financial advisor at one of the top five financial advisory firms in the world. Your firm constantly competes with the other major firms to manage and automatically trade assets in a highly dynamic environment. In recent years, your firm has heavily profited by using computer algorithms that can buy and sell faster than human traders.

The speed of these transactions gave your firm a competitive advantage early on. But, people still need to specifically program these systems, which limits their ability to adapt to new data. You’re thus planning to improve the existing algorithmic trading systems and maintain the firm’s competitive advantage in the market. To do so, you’ll enhance the existing trading signals with machine learning algorithms that can adapt to new data.

## What You're Creating

You’ll combine your new algorithmic trading skills with your existing skills in financial Python programming and machine learning to create an algorithmic trading bot that learns and adapts to new data and evolving markets.

In a Jupyter notebook, you’ll do the following:

* Implement an algorithmic trading strategy that uses machine learning to automate the trade decisions.

* Adjust the input parameters to optimize the trading algorithm.

* Train a new machine learning model and compare its performance to that of a baseline model.

As part of your GitHub repository’s `README.md` file, you will also create a report that compares the performance of the machine learning models based on the trading predictions that each makes and the resulting cumulative strategy returns.

## What was done ?

Used the starter code file to complete the steps that the instructions outline. The steps for this Challenge are divided into the following sections:

* Establish a Baseline Performance

* Tune the Baseline Trading Algorithm

* Evaluate a New Machine Learning Classifier

* Create an Evaluation Report

### Established a Baseline Performance by doing the following

Used the provided starter code to establish a baseline performance for the trading algorithm. To do so, completed the following steps.

In the Jupyter notebook. Restarted the kernel, ran the provided cells that correspond with the first three steps, and then proceed to step four.

1. Imported the OHLCV dataset into a Pandas DataFrame.

2. Generated the trading signals using short- and long-window SMA values.

3. Split the data into training (X) and testing (y) datasets.

4. Use the `SVC` classifier model from SKLearn's support vector machine (SVM) learning method to fit the training data and make predictions based on the testing data. Review the predictions.

To achieve this, the X and y datasets were scaled using StandardScaler() function

![](ScaledData.png)

Then, the data was subjected to prediction using SVC classifier model from sklearn.+svm

![](SVC.png)

5. Generated and Reviewed the classification report associated with the `SVC` model predictions.

The accuracy was pretty low at 56%

![](SVC_CR.png)

6. Created the predictions DataFrame that contains columns for “Predicted” values, “Actual Returns”, and “Strategy Returns”.


7. Create a cumulative return plot that shows the actual returns vs. the strategy returns. Save a PNG image of this plot. This will serve as a baseline against which to compare the effects of tuning the trading algorithm.

Created the cumulative returns plot with 3 months of data with 4 days short-window and 100 days long-window as specified in the starter code

![](CumPlot_3Mon.png)

8. Write your conclusions about the performance of the baseline trading algorithm in the `README.md` file that’s associated with your GitHub repository. Support your findings by using the PNG image that you saved in the previous step.

Classification Report showed pretty low accuracy rate which is 56%. The plot says - The Actual Returns were lower compared to the Strategy Returns going into 2021

### Tune the Baseline Trading Algorithm

1. Tuned the training algorithm by adjusting the size of the training dataset. To achieve this, the data was sliced into 6 and 12 month periods. 

Below are the results :

The results for the 6 months window with 4 day short-window and 100 days long-window

![](CumPlot_6Mon_4SW_100LW.png)

The results for 12 months window with 4 day short-window and 100 days long-window

![](CumPlot_12Mon.png)

What impact resulted from increasing or decreasing the training window?

Resizing the training window to 6 months fetched better results.

2. Fruther Tuned the trading algorithm by adjusting the SMA input features. Adjust one or both of the windows for the algorithm. 

Adjusted the Short and Long windows for 6 months training dataset..

First reduced the Long Window to 60 days..

Results for 4 day short-window and 60 day long window

![](CumPlot_6Mon_4SW_60LW.png)

Increased the short window to 10 days and increased the long window to 200 days, below are the results.

![](CumPlot_6Mon_10SW_200LW.png)

Answer the following question: What impact resulted from increasing or decreasing either or both of the SMA windows?

Adjusting the one of both of the windows did not fetch any better results.

### Evaluated a New Machine Learning Classifier

1. The original parameters from the starter code were used and ADA Boost classifier was used for prediction. 

Imported the ADA Boost Classifier+

![](ImportADABoostClassifer.png)

Fit the original scaled training and predict using the original test data

![](ADABoost-Fit-Predict.png)


3. Backtested the new model to evaluate its performance.

Generated the Classification Report

![](ADA-Boost-Classification-Report.png)

 Generated the plot of the cumulative product of the actual returns vs. the strategy returns

![](ADA-Boost-Cumulative-Returns.png)

Answer the following questions: Did this new model perform better or worse than the provided baseline model? Did this new model perform better or worse than your tuned trading algorithm?

ADA Boost cumulative returns graph show a slightly better results compared to the one generated using SVC with no major difference. However, looking at both the classification report, the accuracy percentage remains low around 55%.

### Create an Evaluation Report

In the previous sections, you updated your `README.md` file with your conclusions. To accomplish this section, you need to add a summary evaluation report at the end of the `README.md` file. For this report, express your final conclusions and analysis. Support your findings by using the PNG images that you created.

---

## Submission

* Use the started code provided to create the machine learning trading bot and host the notebook and the required files.

* Include a `README.md` file with your conclusions as requested.

* Submit the link to your GitHub project to Bootcamp Spot.

---

© 2022 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.
