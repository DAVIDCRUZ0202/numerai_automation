# Model Building

For model development, we cover the entire process from pre-processing, to model implementation, metrics, and refinement. I recommend reading through the actual notebook where I write about the technical results of each process. It holds many more insights which I do not share in this readme. If you're on a time crunch then just read through this readme and you should still get the summary of the work that has been done 😄

## Data Preprocessing
Since this data has already been cleaned, we don't have to any vital data pre-processing. The process of cleaning and obfuscating the data is covered in detail [here](https://docs.numer.ai/community-content/understanding-numerai/numerai-structure#user-models). For the sake of our competition submissions, I created a small data cleaning function which takes in the training data and returns a train / test split which is ready for training and testing with models.

<img src="assets\1.clean_data.png" alt="cloud_signup" width="200" height="200">

## Evaluation Metrics
This competition is scored based on a variety of evaluation metrics which are explained in detail [here](https://docs.numer.ai/tournament/true-contribution-tc) [here](https://docs.numer.ai/tournament/metamodel-contribution) and [here](https://docs.numer.ai/tournament/feature-neutral-correlation). All of these methods have unique qualities to them, but a universally agreed upon method for gauging model performance is the [spearman's correlation](https://forum.numer.ai/t/pearson-vs-spearman-scoring-confusion/2559/2) coefficient and regular coefficient of correlation. I score my models with these metrics as well as including the r2 score which serves to show which models are working to predict actual values rather than just random information.

<img src="assets\2.evaluation_metrics.png" alt="cloud_signup" width="200" height="200">

## Model Implementation

To prove the concept of automation with ibm cloud, I initially fitted and predicted with a simple linear regression model. I follow this by creating a function which tests a larger number of pre-built algorithms to observe the general performance of all of these different models. By observing the performance of these models, I can make more specific choices as to what I want to incorporate and what I can exclude from my research.

<img src="assets\3.func_1.png" alt="cloud_signup" width="200" height="200">

## Refinement
After observing initial results, I used a similar function to examing some more results from some more advanced algorithms. This process produced some of the best model choices available to me, and I was able to take some more precise decisions in what my final model would look like.

<img src="assets\4.func_2.png" alt="cloud_signup" width="200" height="200">

## Model Evaluation and Validation

So with the final choices in hand, for a final pass at model choice, I created a cross validation pipeline to choose the best hyperparameters for my model. This ensured that without any additional feature engineering, I am using a model which is dependable in it's ability to make predictions. This final model from the cross validation process is the model that will stay with my project for a long time.

<img src="assets\5.cross_val.png" alt="cloud_signup" width="200" height="200">

## Justification
After testing the final model, we find that we almost double our correlation metric from our original OLS regression model. We ended up with a gradient boosting regressor, and so we can see the improvements in our product as a result of using a model which accelerates learning on gradients which show steeper curves and also the fact that we are using decision trees which provide predictions of values instead of a single regression line, as is found in regression.

## Reflection
Upon completing this workflow , I see a lot of potential for improvement. I am overall very happy that I am able to contribute the novel workflow of automating this process with IBM Cloud at no cost to users. I believe that my solution to  automation is actually a more streamlined process of what is available with AWS and the CLI, thanks to the power of notebook jobs from IBM's CP4D platform. Hopefully this workflow inspires more practitioners to deploy their own solutions and to continue to build upon the results of those deployments.

## Improvement
=Besides defining my evaluation metrics, I have really not spent much time researching the available knowledge from numerai's community. Some next steps include spending more time with the numer.ai community to share insights as well as to learn a lot more from what they have to offer. There has been a plethora of material and ideation taking place within their forums and I highly recommend anyone interested to explore their archives. For immediate next steps for my project, improvement is definitely possible with some advanced feature engineering. Engineering features to consider some features more heavily than others, or considering some eras more heavily than others will surely prove to show some different outcomes. Thankfully this competition provides me with the perfect place to practice and enhance my skills.
