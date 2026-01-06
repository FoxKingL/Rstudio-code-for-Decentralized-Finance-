# Rstudio-code-for-Decentralized-Finance-
My course work for MATP 4910 during Fall 2024

Overall, all of my code is related to classi cation models, also some code for smote results with in terms of some imbalanced datasets, mainly the event pairs with liquidations.
For data processing, we get the datasets from our survival data folder based on di erent index event and outcome event.
For index events, we have Borrow/Deposit/Repay/Withdraw. Besides, for outcome events, we have Account Liquidated/Liquidation Performed/Deposit/Repay/Withdraw/Borrow. We consider each di erent index event and outcome event as a pair, such as “Borrow” and “Repay”, “Deposit” and “Borrow”. For our classi cation, we need to apply survival analysis and turn the given datasets into a binary problem based on the time threshold. 
After the process, the binary event column will be “event” with “yes” or “no”. In order to make the dataset events more balanced, we use cutoff days as time threshold based on RMST calculations. In general, we will have 16 di erent pairs in total. (We drop all the event pairs that contain “liquidation performed”) 
We run the all the models we have based on the datasets after processing. Our model includes Logistic Regression, K nearest neighbor, Random forest, Decision Tree, Naive Bayes, XG boost, ADA boost, GBM, Elastic Net. 
We compared the results of each model and try to conclude which model is the best.
We checked the percent of event for each event pair, we found that some datasets are unbalanced. To x that problem, I use the SMOTE function in our pipeline to balance our train dataset and use the new dataset to train the model. Then I will test trained model on test dataset to check if we get better balanced accuracy****
