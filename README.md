
### `Job Recommendation System`

Team - Adithi, Pavan, Manaswini, Dinuka

**Problem Statement:**

People are interested in thinking of their next stop as in whether they go to a new company, a problem that exists is that there's no certain way of knowing which options would best fit, based on the current profile of the person. We are going to utilize data from Linkedin profiles which may be able to train a machine learning model to make recommendations of the next company.


Hence , the goal is to build a recommendation system that will help predict the possibility of a student/ employee getting into a certain company based on their profile and the profiles of the current employees of that company.

#### `Data`:

We have a small dataset which we found on kaggle, We plan to augment the same dataset with numerous records.
https://www.kaggle.com/heet9022/linkedin-dataset

##### `Model`:

We plan to use DNN Multiclass Classification to train the model. Multi-label classification involves predicting zero or more class labels. We may collect the unique set of companies in the dataset and use that as the number of neurons in the output layer. The assumption we make here is that the output label is a function of inputs. 


Softmax assigns decimal probabilities to each class in a multi-class problem. Those decimal probabilities add up to 1.0. Hence, we plan to use Softmax  as activation function, this would be useful in predicting the probability of a person getting into each of the set of unique companies. 


We could display the company with the highest probability assigned by softmax. 


We plan to start with two hidden layers in the architecture, and keep adding until the performance of the model deteriorates. 


To avoid overfitting, we plan to incorporate ‘dropout’ and/or ‘early stopping’ regularization techniques.

##### **`Evaluation`**:

For judging the performance of the model, we plan to use evaluation metrics such as mean squared error, root mean squared error, gini, entropy etc.

##### **Addressing the comments posted on our initial project proposal** :

**How exactly will you collect the data? What will the data consist of exactly? How much data can you collect, since there generally are limits to this using social media?** 


For now, we are planning to take a dataset that is available on Kaggle. We’re in a dilemma about data extraction from linkedIn, as we read it was illegal on reddit. If it’s legal, we could perform web crawling to get the data but there as it was mentioned, there would be a limit on how much we can extract. So, we were thinking of performing something like data augmentation so that we have more data and train our model well.


**What exactly is the label and how is it determined? I'm not sure what "what's next" means as it pertains to labels. Also, how do you compute the "possibility of a student" getting into a certain company? Where will the labels for this come from?**


Regarding “what next” means. We were planning on modifying the problem statement a bit. Instead of doing it from a student’s point of view, we plan to do it from a working professional’s/ student’s point of view. so, the target label would be the ‘company name’ of the next company that he/she would most likely get into.



**A linear regression model on its own is likely not enough to get meaningful results. What other learning algorithms will you try if this is the case?**

To compute the probability of a person getting into a certain company, we plan to use softmax activation function, which would give us the probability for each company. The class having the highest probability is the company that this person most likely might get into.
We plan to use DNN multiclass classification techniques.


**How will the work be divided amongst the four of you?**

Dinuka and Pavan will be working on the data pre-processing part whereas Adithi and Manaswini will work on training the model and evaluation.


**`What we have done so far:`**

We have analyzed the dataset, and attributes are, category(HR, designing, management etc), linkedIn profile URL, profile picture, description( position, role),  experience(company name, duration, title, employment date), name, position (current position, company name), location, skills.

We have made an attempt to clean the dataset, the attributes experience, position and skill, contain english sentences. 

We plan to split it into a list of words, and put it into columns so that each of those words can be assigned individual weights that contribute to overall prediction of target labels.


