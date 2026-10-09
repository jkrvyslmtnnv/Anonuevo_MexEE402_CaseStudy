# -Anonuevo-_MexEE402_CaseStudy
# MexEE 402: Data Preprocessing Case Study

MexEE Elective 2: Data Science and Machine Learning
Batangas State University, Alangilan Campus
1st Semester, AY 2026-2027

## Member

| Name | Student Number | Section |
|---|---|---|
| Añonuevo, Jake Arvey | 23-07049 | MEXE 4102 |

## Notebook links

| Chapter | Member 1 |
|---|---|---|
| Ch1_2_3 | [link](https://colab.research.google.com/drive/1MRZ5uOrLqHXaJl3Uirhqr1kiyPh0xnpx?usp=sharing) |
| Ch4 | [link](https://colab.research.google.com/drive/1cbKv8F5eABV6KanksFvlz8VE0quBMZRB?usp=sharing) |
| Ch5 | [link](https://colab.research.google.com/drive/1n9aP1NuSBDseXIiv8S3EkhKZ78zpOrdj?usp=sharing) |
| Ch6 | [link](https://colab.research.google.com/drive/1a0OQ_60SjgJsjNUG4ywU3IRbS80HASHX?usp=sharing) |
| Ch7 | [link](https://colab.research.google.com/drive/1Ise30r8294NkTdQjOPW5SdlVV0YpsiZQ?usp=sharing) |
| Ch8 | [link](https://colab.research.google.com/drive/1e8X6-0j-0FPJy9xzCpaxW3JdG89y74N6?usp=sharing) |
| Ch9 | [link](https://colab.research.google.com/drive/1nMMQZIoufTo1kIB62n4zwCkC3UbTCsav?usp=sharing) |

## What I learned

One short paragraph per chapter, Ch1_2_3 to Ch9. Say what the chapter taught
you and what surprised you. Not what the library does, but what you understood.

Ch1_2_3: In chapters 1, 2 , and 3, taught me that it is possible to process data using prompts making data processing much easier just by having correct and available data. Chapter 1 - Data preprocessing, in the word pre- signifies the actions that is done before processing the data. For the chapter 2 - The power of Data, is the possibilities made as to having data, which can be in different formats, an essential part of data preprocessing, using import pandas as pd. For the Chapter 3 - Cleaning your Data, is to clean or fix the data such as using imputation, deletion, and prediction

Ch4: For Chapter 4 - using the data into others ways or application, where importing pandas as pd allows and having inputing a simple raw data, I can create new features, such as using the values then applying formula to get a new sets of data. Another application is creating a category where ranges are formed for easier understanding, interaction features, polynomial features, categorical variable encoding, and ordinal coding. To sum up, chapter 4, explains the other applications and possibilities by having data, it can be tailored or be categorized onto what data is needed.

Ch5: Chapter 5 - Data Scaling and Normalization, in this chapter what taught me is for the data to be processed fairly. Data can have different ranges but by Data Scaling, use of Z-Score standardization, and MinMaxScaler, the data can be scaled fairly so the data is useful depending on the purpose and use of data, depending also on the algorithm's requirements

Ch6: Chapter 6 - Dealing with Outliers, Explained. Outliers are the data that is out of range compared to others, this chapter tackles ways to deal with it. Detecting outliers by Z-score or Interquartile Range. Use Z-score first, then for more accurate results is to use Interquartile Range. Strategies to use are Capping & Flooring which replaces extreme values with the nearest boundary, Log Transformation to compress large values so inaccurate data becomes more balanced, lastly is removing outliers which deletes the extreme values

Ch7: Chapter 7 - Feature Selection taught me the correlation or how to variable are related which both can increase or decrease together, also called positive correlation. Negative correlation where opposites occur, where one increases while the other decreases, and zero for unrelated variables. Correlations can be implemented by import pandas as pd, using df.corr() to compute correlations

Ch8: Chapter 8 - Constructing a preprocessing pipeline, taught me that automation can be set or made which can be used for the next set of data, which can be done by simply importing a data file, but first the pipeline needs to be coded for the data to be preprocessed, automated for it to be sequential and reliable, not manual, time consuming, and error-prone

CH9: Real-World Application - Data Preprocessing taught me the use of coding or preprocessing applied in a scenario, where having a raw data can be processed into an accurate data, then compressing, and removing irrelevant features for unnecessary information. Then the evaluation, for the data quality report to know if there is none missing as well as the visualization for better understanding.

## Errors I found

List any mistake you found in the original notebooks, and the correct version.
There are real ones in there. Finding them earns points.

Chapter 1_2_3: inplace=True warning: breaks in pandas 3.0. Fix: df['Year'] = df['Year'].fillna(df['Year'].mean()) Mean Year (2006.4): not a real year. Fix: use median, then .astype(int) Mode for Publisher: creates false data. Fix: fillna('Unknown') notna() deletion: nothing left to delete after imputation. Fix: run it instead of imputing, or use dropna(subset=['Publisher']) Duplicate check with Rank present: Rank is unique, so duplicates can’t show. Fix: drop Rank first Hardcoded 40 cutoff: removes real top sellers. Fix: justify it or use IQR Unused numpy: remove it Missing pandas import cell: causes NameError. Fix: add import pandas as pd Gapped index: Fix: df.reset_index(drop=True)

Chapter 4: Empty ordinal cell: no code. Fix: df['Ice Level'] = df['Ice Level'].map({'Little':1,'Medium':2,'Lots':3}) Binning drops 70: pd.cut excludes the lowest value, so it becomes NaN. Fix: add include_lowest=True. Ice Cubes list: it must have exactly as many values as df has rows, or you get a ValueError. Fix: check len(df). Missing import: pd isn’t defined, so you get a NameError. Fix: import pandas as pd at the top. Typo: 'Temperature Sqaured'. Fix: rename it to 'Temperature Squared'. One-hot shows True/False: not 1/0. Fix: add dtype=int to pd.get_dummies.

Chapter 5: Missing import. StandardScaler is used, but only MinMaxScaler is imported. Missing code for the MinMax output. The cell only has df_2.head(), but the output shown is a 0 to 1 array. Add scaler = MinMaxScaler() and print(scaler.fit_transform(df_2)).pd and df aren’t shown. import pandas as pd and the first DataFrame (df) need to appear earlier in the notebook, or the StandardScaler cell will crash.

Chapter 6: Z-score missed 100. The notes call it a “clear outlier,” but the code found none. Its z-score was about 2.6, below 3.
“Again” is wrong. Only the IQR method caught 100. Z-score did not. Dataset too small. With 8 values, a z-score can never reach 3. Log transformation claim is too broad. It only helps right-skewed data, and it can’t be used on zero or negative numbers.
Minor issues. IQR by hand is 9.5, but pandas gives 9.25 (different method, not a real mistake). data is reused for two different types. “Double-click (or enter) to edit” is leftover Colab text.

Chapter 7: The text contradicts the data (Correlation section). The wrapper section’s code is missing. The filter result is not carried through to the other methods.

Chapter 8: Data leakage: preprocessing runs on all of X before a train/test split. Columns dropped: ColumnTransformer keeps only Age and Fare by default. No encoding: Sex and Embarked are text and need encoding. Useless columns kept: Name, Ticket, PassengerId, Cabin should be dropped. Misleading title: Step 3 only separates X and y; it’s not a train/test split. Wrong claim: reuse on new data needs .transform(), not .fit_transform(). Minor: Fare has no missing values, and median suits Age better than mean.

Chapter 9: Missing steps: The intro promises a log transform on Fare and Cabin handling, but the code does neither. Fix: add np.log1p to Fare in the pipeline, and either drop Cabin on purpose or create a HasCabin column. Wrong histogram column: titanic_preprocessed[:,2] is Embarked_C, not Age. Fix: use titanic_preprocessed_df['num__Age'] (and call it “scaling,” not “discretization”). Age overwritten: data['Age'] = pd.cut(...) replaces the numbers with labels, which breaks later plots and the heatmap. Fix: save to a new column, data['AgeGroup']. Incomplete quality report: Only the “after” missing values are printed. Fix: also print data.isnull().sum() before preprocessing. Empty Steps 1 and 2: The Drive mount, imports, and pd.read_csv are missing from the export. Fix: add them back so the notebook runs. Data leakage (best practice): The pipeline is fit on the whole dataset. Fix: split train/test first, then fit_transform on train and transform on test.


## Note on AI tools

Say whether you used an AI tool, and what for. This is not a penalty.
Hiding it is.

What I've used during running the program or the generating codes is Gemini, where codes can be generated just by simply making a prompt for Google Gemini to create data, simply from an example to a real one.

For understanding and determining the function as well as the errors of the code is where Claude is used, understanding what are the functions of the code and other possibilities, though not being able to retain the information provided wholly, however it allowed me to understand even for a brief understanding

## References
For datas: https://www.kaggle.com/

McKinney, W. (2021). Python for Data Analysis, 3rd ed. O'Reilly.
VanderPlas, J. Python Data Science Handbook.
Any other page or article you used.
