# sissejuhatus-andmeteadusesse-projekt
Link to our Android application repository https://github.com/AnneliKlamas/Andmeteaduse-pp

our project starts with imports. after that is getAndmed(), which uses the Open Data link to import our data.

tabel_andmetest() creates a dataframe from the getAndmed() data. there we define dataframe columns and redefine some data ("decision_not_ok" to 0) so we can analyse it easier later. we write the data from getAndmed() into the columns and after that we write them into the dataframe, which we return.

we use three modules in this project: decisionTree(), randomforest() and knn().
for all three we begin by narrowing the data down to columns we need. we get rid of null "status"es to not mess with the end prediction. after that we define X, y and training and testing datasets. We also overwrite labels for easier data analysis. we train the data by using the fit() function. and then return the prediction by using the predict() function.

regressionLog() is much the same but it instead returns the prediction's "score", how certain we are in our prediction.

arva(arvamiseks) and arvaLihtandmed(kategooria, summa) are related. arvaLihtandmed(kategooria, summa) puts the the user input of the category and sum into a dataframe to call out arva(arvamiseks). arva(arvamiseks) first renames labels for easier analysing and then calls out a module, after which it calls out predict(user input), so the trained module can predict what it thinks the input's answer would be.

biggestFunding() and smallestFunding() are also quite similar.
they start by calling out tabelAndmetest(), then define min/max of certain columns (discounting 0), and return the min/max's applicationround_title, approved_amount, managing_organization_name, name and project_name.

our last cell depicts our program (for PC). it has 4 tabs, one for information about us and the project, one about predicting data using arvaLihtandmeid(), one for biggestFunding() and one for smallestFunding().
