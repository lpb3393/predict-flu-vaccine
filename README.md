# Business Understanding

Vaccines are crutial in many ways but most importantly because they can prevent or reduce the severity of many infectious diseases that can cause serious illness, disability, or death. By vaccinating a large proportion of the population, the spread of the disease can be slowed down or stopped, which protects not only the vaccinated individuals but also those who are not vaccinated or cannot be vaccinated due to medical reasons, through herd immunity. Vaccines are one of the most effective and cost-effective public health interventions that have saved millions of lives and improved the quality of life for many more.

The business problem I wanting to solve is can we predict who will recieve the H1N1 vaccine given information that was collected from the National 2009 H1N1 Flu Survey (NHFS). I also want to make recommendations to Pfizer on how they can maximize the number of people to get vaccinated in the future.

# Data Understanding

The National 2009 H1N1 Flu Survey (NHFS) was sponsored by the National Center for Immunization and Respiratory Diseases (NCIRD) and conducted jointly by NCIRD and the National Center for Health Statistics (NCHS), Centers for Disease Control and Prevention (CDC). The NHFS was a list-assisted random-digit-dialing telephone survey of households, designed to monitor influenza immunization coverage in the 2009-10 season.

The target population for the NHFS was all persons 6 months or older living in the United States at the time of the interview. Data from the NHFS were used to produce timely estimates of vaccination coverage rates for both the monovalent pH1N1 and trivalent seasonal influenza vaccines.

## Data Preparation

After exploring the datasets, I thought the best approach would be to join the two together. That way I can look to see how how each variable correlates to whether or not a person got the vaccine and then further prep the data for analysis all together.

# Exploratory Data Analysis

In this section, I wanted to first compare the proportions of people getting vaccinated. I then wanted to see how many Null values were in the dataset and fill those blank values with the columns "mode." Then to prep the data for modeling, I split the data between a training set and a test set, using a Train Test Split. This allows for the model to train on the dataset but when running the analysis on the test set, it is new data the model hasn't seen.


# Modeling

In this section, I wanted to first compare the proportions of people getting vaccinated. I then wanted to see how many Null values were in the dataset and fill those blank values with the columns "mode." Then to prep the data for modeling, I split the data between a training set and a test set, using a Train Test Split. This allows for the model to train on the dataset but when running the analysis on the test set, it is new data the model hasn't seen.


# Evaluation

The baseline decision tree model was slightly improved by the final model. Since the values in the dataset were binary, I felt that precision was the best metric to go judge the model performance by. Initially the precision value for 0 was 0.87 and the slightly decreased in the final model to 0.86. The precision value for 1 was significantly improved by the value, changing from 0.68 to 0.74. Running the dataset through the Random Forest Classifer and then again after the Grid Search, ultimately improved the models performance. The final model did do slightly better on the training data than the test data, possibly suggesting that there could be some slight over fitting.


# Limitations

A major limitation with this dataset was that there was a significant amount of null values. To prep the data for the model, the null values were replaced but this could affect the overall quality of the data. Also, a relatively small number of people were polled for this survey. In the future, it would be beneficial to get a larger number of people to particiate and give their feedback.


# Recommendations

My first recommendation to increase the number of people who get vaccinated is to partner with doctors across the country. The model showed that Doctor Recommendations significantly influenced the results and when directly comparing doctor recommendations to those who did or did not get the vaccine, it showed that when it was recommended the patient was more likely to get the shot. Doctor recommendations are one of the most influential factors that can increase the number of people who are vaccinated. People trust their doctors as credible and reliable sources of information and advice about their health. Doctors can educate their patients about the benefits and safety of the vaccine, as well as the risks and consequences of not getting vaccinated. Doctors can also address their patients’ concerns and questions, and dispel any myths or misinformation they may have heard. By providing personalized and tailored recommendations, doctors can motivate their patients to make informed and confident decisions about getting vaccinated

Since the data also showed that with people's increase in knowledge about the vaccine, they were more likely to recieve it, my second recommendation would be to implement a marketing campaign that puts out a PSA nationwide. A public service announcement about getting the vaccine is a powerful way to educate people about the virus and encourage them to protect themselves and others. It could provide factual and reliable information about how the virus spreads, what are the symptoms and risks of infection, and how the vaccine works and why it is safe and effective. A PSA can also address common myths and doubts about the virus and the vaccine, and use persuasive techniques such as emotional appeals, social norms, and incentives to motivate people to get vaccinated. By using clear and simple language, visual aids, and credible sources and messengers, a PSA can help people understand the benefits and importance of vaccination and reduce vaccine hesitancy.


# Next Steps

Something that would be interesting and informative would be to see how this data compares to COVID-19 respondes. Conducting a new survey and seeing how people's responses have changed or stayed the same from 2009 would be important infomation to have if another pandemic were to hit the United States. Comparing H1N1 vaccination rate to COVID-19 vaccination rate can be important for understanding the factors that influence vaccine acceptance and coverage, as well as the impact of vaccination on the pandemic outcomes. Comparing the vaccination rates can also help evaluate the effectiveness of vaccinations, as well as the emergence of new variants. By analyzing the similarities and differences between the two pandemics and their vaccination campaigns, Pfizer could learn from the past experiences and improve the current and future responses to infectious disease outbreaks.

## For More Information
See the full analysis in the [Jupyter Notebook](https://github.com/lpb3393/predict-flu-vaccine/blob/main/predict-flu-vaccines.ipynb) or review the [presentation](https://github.com/lpb3393/Home_Renovations/blob/main/Home%20Renovations%20Presentation.pdf)

```
├── photos
├── .gitignore
├── Home Renovations Presentation.pdf
├── Home Renovations.ipynb
└── readme.md
```