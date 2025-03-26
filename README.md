# IGP-Premier-League
All code used in our IGP project on investigating Premier League final standings.

## Scripts in chronological order:
- 1.Combining All Csvs
- 2.Relegated Teams Stats
- 3.Comparing Relegated and Survived Shots
- 4.First Machine Learning
- 5.More Metrics
- 6.More Metrics Partial Data
- 7.Gradient Boost
- 8.Model Selection using K-Fold
- 9.Gradient Boost CV

## Quick Explanation of what the scripts do:
- 1.This is the first script that was needed when we gathered all documents, one document by season. We had to merge all documents into one and this has been done using this script.
- 2.This script allowed us to create a new sheet in our main excel document, holding stats of relegated teams only.
- 3.We then wanted to explore ratios, initially investigating the ShotsOnTarget/Shots ratio, to later include it as a feature for ML. This has finally not been used as we decided to take a different approach.
- 4.This was the first attempt to a machine learning model, here a Random Forest as by intuition we thought it would be suited for our proble. The model obviously lacked features and was trying to predict if the team was relegated or not only. Hence, not a really meaningful result.
- 5.And6.More metrics were definitely needed as we needed more features for our model to be meaningful. These scripts are hence here to create as many features as possible that would allow the creation of more columns in the "Season Summary" sheet. There are two scripts becausethe first one does the computation for all past data (1993-2024) whereas the second does the same calculations but for the current 2024-2025 season which is not over yet.
- 7.After a little bit of playing around and reading articles on Machine Learning, we realised that boosting algorithms were more suited for our analysis. This is a script training a Gradient Boost algorithm on the newly created features thanks to 5. and 6., to then predict final standings of the Premier League teams in the 2024-2025 season.
- 8.K-Fold Cross Validation was then performed to ensure we were training and using the most optimised setup for our model.
- 9.The same Gradient Boost as 7. but including Cross Validation for more robustness.
