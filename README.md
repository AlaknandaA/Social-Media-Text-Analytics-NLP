# Social-Media-Text-Analytics-NLP
To gauge the popularity of a product using Text analytics

My customer is a mobile manufacturer based in the US, which entered the market three years ago. As they are a new entrant in the sector, they want to understand their competitors and preferences of their users so that they can design their strategies accordingly. They want to tweak the marketing strategies to add more value to their brand, provide features to customers that add the most value, and close the demand-supply gap. Their objective is to increase the market share as well as the brand value.

As a data analytics provider, I have been approached by this mobile phone manufacturer. They want me to provide them with some major insights into the mobile phone industry to help them achieve their objective. Their objective is to develop a new product optimally and create some marketing strategies.

### Data
The data is huge and unstructured. It is taken off an e-commerce site. I have two main files- metadata file and phonedata file.

#### Metadata
Contains characteristics of all products present on the e-commerce website like their unique Id, cetegories, rank, brand, details, etc. There are a lot of nulls.

#### Phonedata
Contains customer reviews and customer ratings data for each product. Can have more than one customer review for one product. Has features like overall rating, review text, summary, reviewer name etc. The data does have some nulls, but more than that, it is very unstructured, especially the review text data is fully textual and has a lot of errors and inconsistencies.


### Data Cleaning and preprocessing:
After importing both files, they have been cleaned. Metadata file took a long time to clean because it has lots of nulls, feature_engineering etc. Also checked for duplicate values and removed them. <\br>
Phonedata doesn't have lot of nulls and not much cleaning can be done at column level at this stage.

### Text Analytics:
1. Performed textual analytics using regular expressions to remove punctuation marks and other useless characters, removed stopwords- on the review text in phonedata file.
2. Used tokenization to create word tokens. After this, performed lemmatization on the data to reduce the words to their roots.<\br>
3. Also merged the two files Metadata and Phonedata based on the unique product identifier field.<\br>
4. Extracted features from positive reviews, these are the features that customers want to see in future phones.
5. Extracted negative features also, these are the ones which company needs to avoid or look out for.
6. Extracted keywords for positive features, these are the exact features that customers want to see being implemented in future phones.

### Visualization and Storytelling:
1. Also built visualisation showing market share of competitors- so our client can know who to keep and eye out for in the market.
2. Created wordclouds for both positive and negative features.
3. Created a presentation for stakeholders and presented it to them for decision making.

### Model Building:
Built a Naive Bayes model for predicting review label on the train data and fitted it to the test data with an AUC score of 77%.
