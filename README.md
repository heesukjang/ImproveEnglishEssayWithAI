# Project Overview
###### <i>UC Berkeley MIDS `Natural Language Processing with Deep Learning` Group Project</i>

### Objective: 
The goal of this project is to develop an Automated Essay Scoring (AES) system utilizing Natural Language Processing (NLP) technologies to autonomously grade argumentative essays, specifically targeting English Language Learners (ELLs) in grades 8 to 12. Current automated feedback tools often fail to provide feedback tailored to a student's language proficiency, which can result in biased evaluations. Our AES system is designed to enhance these tools by offering more personalized feedback to better support the unique needs of ELLs.

### Scoring Criteria:
The AES system evaluates essays across six key analytical dimensions: cohesion, syntax, vocabulary, phraseology, grammar, and conventions. Each dimension reflects a specific aspect of writing proficiency, with scores ranging from 1.0 to 5.0, in increments of 0.5, where higher scores represent greater proficiency.

### Technical Approach:
WWe employed both **BERT (Bidirectional Encoder Representations from Transformers)**, trained on formal text, and **BERTweet**, trained on informal language such as tweets, to assess student essays. These models capture both semantic nuances and structural elements, mapping linguistic features to scores in an ordinal framework. To enhance scoring precision, we used **Mean Columnwise Root Mean Square Error (MCRMSE)** regression loss, ensuring a more accurate and consistent scoring range.

### Performance Enhancement Techniques and Performance Results:
Starting with a frozen BERT-base-cased model as a baseline, we experimented with unfreezing various numbers of lower layers and adjusting hyperparameters on both BERT and BERTweet to allow the models to learn from different usages of English during training. We also applied clustering and stratified k-fold cross-validation to check for patterns in score distributions and to ensure our model generalized well across different data partitions, particularly at the lower and higher ends of the scoring scale.

However, since the analytical measures followed a normal distribution, applying K-means clustering and k-fold cross-validation did not significantly enhance model performance. Our best result was a moderate MCRMSE loss score of 46%, achieved with 12 trainable layers in the BERT transformer model.

For more details on the teamwork, please refer to the link below:
* [Team GitHub](https://github.com/srilamaiti/spring_2023_w266_final_project_heesuk_iris_srila/tree/main)


