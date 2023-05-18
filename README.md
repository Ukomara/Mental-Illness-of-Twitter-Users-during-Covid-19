# Mental-Illness-of-Twitter-Users-during-Covid-19
### Introduction :
Acceptance and understanding of mental illnesses have gone a long way from where they used to be, but there is always room for improvement. Mental illnesses should be treated in the same way as physical illnesses. I believe they are closely linked. These two cannot be separated because the entire body is linked and connected. The brain is an organ like any other in the body, and it may be affected just like any other. When the brain is sick, it doesn't only affect the brain; it affects the entire body and general well-being. Substance addiction, self-harm, and suicide are all prevalent and harmful behaviors among those who suffer from mental illnesses. The stigma associated with mental illness prevents people from seeking the treatment they require and drives them to hide their suffering.
Through the rise of social media in recent years, the Internet has gained a broader scope. The social network is now, more than ever, a medium for communication and information sharing. As a result, studying user patterns through social media sites is intriguing. It provides excellent content for eliciting the emotions of users through their postings. This study intends to conduct a comparative study of two types of mental illness, PTSD (Post-traumatic stress disorder) and Depression, to better understand key phrases used by users with mental illness. Although they sound similar there are different.

### Post-traumatic stress disorder:
PTSD is a disorder in which people have trouble recovering after watching or experiencing a traumatic incident.

### Depression:
Depression is a term used to describe a range of illnesses that affect a person's mood, such as depression or bipolar disorder.
Research Question:
 What are some of the recurring topics in user-posted content concerning 'PTSD' and 'Depression'? Is there a common pattern of words in the topics they try to address?

### Method: 
### Data:
The data for this study was gathered via the Twitter platform. The data is acquired via the Twitter API. Because this study focuses on mental illness following the pandemic, the data collected covers the years 2020 to the present. To investigate the mental illness of Twitter users, "PTSD" and "Depression" are two key terms that have been used to collect tweets. For this study, a total of 1000 tweets were gathered, including 500 tweets containing the phrase "PTSD" and another 500 tweets containing the keyword "Depression." The gathered tweets are divided into two CSV files and cleaned before being analyzed further.

### Analysis:
Automatically extracting what topics people are talking about from enormous amounts of text is one of the fundamental applications of natural language processing. It is beneficial to know what individuals are talking about and to comprehend their issues and viewpoints. And personally reading through such vast volumes and compiling the topics is difficult. This study makes use of the Gensim package's Latent Dirichlet Allocation (LDA).
LDA takes a proportional approach to topic modeling, treating each text as a collection of topics. And each topic is a collection of keywords, proportionately distributed. Once you provide the algorithm with the number of topics, it simply rearranges the topic distribution within the documents and the keyword distribution inside the topics to get a desirable topic-keywords distribution composition.

### Packages :
Regular expressions re, gensim, and spacy. Numpy and pandas for processing and displaying data in tabular format, as well as pyLDAvis and matplotlib for visualization.
 Lemmatization is done after the data preprocessing stage. Lemmatization is the conversion of words to their root words. The benefit is that the overall number of unique terms in the dictionary is reduced. Then Introduce 'Bigrams' and 'Trigrams' as a better way to topic modeling. Bigrams are two words that commonly appear in the same sentence in a text. Trigrams, on the other hand, are three words that appear frequently. The bigrams, trigrams, quadgrams, and

 others are built and implemented using Gensim's Phrases model. Functions to delete stop words are created when the bigrams, and trigrams model is completed. After you've made your bigrams and trigrams, use lemmatization to call them in order. The LDA topic model's two primary inputs are then generated. The dictionary(id2word) and the corpus are the two inputs taken by the model. Each word in the document is provided with a unique id by Gensim. The resulting corpus is a (word id, word frequency) mapping. The LDA model
 uses this as its input.
 The topic model would be built next in the analysis. Everything we need to train the LDA model is right here. You must also supply the number of topics in addition to the corpus and dictionary. The LDA model for this study is made up of four topics, each of which is made up of several keywords, each of which gives a particular amount of weight to the topic. Each document in an LDA model is made up of numerous topics. However, just one of the topics is usually
 dominating.
 Table 1: Dominant topic and its percentage contribution in each document for “PTSD”
 Table 2: Dominant topic and its percentage contribution in each document for “Depression”
 
### Results:
A word cloud with the size of the words proportionate to the weight is a pleasing sight, even if you've previously seen what the topic keywords are in
  each topic.
The word cloud for "Depression" clearly shows that the keywords are largely the users feelings, with a small contribution of other terms like drug, brain, and medical. But, we may see additional terms other than the users feelings or moods in the "PTSD" word cloud, such as health issue, parent, suffer, watch, people and veteran". It's possible that the trauma that most of the users in the
  data collected experienced these topics.
 After the LDA model has been developed, the following step is to review the generated topics and keywords. This is the final step where we will create the visualizations of the topic clusters. The best tool for visualizing it in a single line
of code is the interactive chart included in the pyLDAvis package.
  visualization shows the distribution of topics in a two-dimensional space.
