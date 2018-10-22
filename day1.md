# Objectives
- Introduce you to data science concepts
- Create a foundation to apply these concepts in Days 3-5

# Agenda
1. [20] Class Setup & Intros & Objectives, Today & Tomorrow
2. [10] Discuss/share - what's your relationship to ML? 
2. [10] What is ML?
3. [10] Why does ML matter to us, to salesforce?
4. [10] How does the data science process work?

5. [10] What is data exploration? Brainstorm.
6. [10] Intro to jupyter notebook 
7. [10] Pandas demo
8. [20] Pandas mechanics, exercises, practice, and debrief
9. [20] TTL demo, exercise and debrief
10. [15] Examining linked data
11. [15] linked data demo, exercise and debrief

12. [15] Explore the rock.csv dataset - any problems?
12. [10] What is data munging? Why is it necessary?
13. [10] Structured/unstructured data, different sources of data, databases

14. [10] Explore the Boston housing dataset
15. [10] What is statistics and why does it matter for us? How useful a tool is it?
16. [10] What's the signifiance of mean, mode, variance, quartiles?
17. [10] Explore the stats and descriptive stats on this dataset... what do they mean?
18. [10] Covariance, causation, correlation

19. [10] What is modeling? 
20. [10] What is model variance? When is it bad? What is model bias? When is it bad?
21. [10] High-level intro to supervised and unsupervised learning, probabilistic vs non-probabilistic models
22. [10] What is probability, why does it matter and how does it work?
23. [10] Probability mechanics and computation exercise
24. [20] Conditional probability, intuition and math
25. [10] Explore setosa

26. [10] Model evaluation - how does that work?
27. [15] What is accuracy, precision and recall?
28. [10] Productionizing the model, reviewing results, testing hypotheses
29. [10] Math, examples for hypothesis testing

30. [15] Q & A


# [20] Class Setup & Intros & Objectives, Today & Tomorrow
- Who am I? 
- What's this class about?
- Who are you?
- How's today and tomorrow look?
- How will the class work? What can you expect?

# [10] Discuss/share - what's your relationship to ML? 
Discuss with your neighbor....

1. What do you know or believe about ML?
2. How is it relevant or irrelevant to you?
3. What do you believe is possible or will be challenging for you with respect to ML?

Let's share.

#  [10] What is ML?
Let's explore together..

- What it is
- What's the purpose of ML
- How does ML benefit us compared to traditional programming
- Why now? 
- Key limitations / enablers

Brainstorm with your neighbor... what are all the examples of machine learning/data science that you see in your lives, in the technology or products you use, etc.


# [10] Why does ML matter to us, to salesforce?
- Brainstorm with your neighbor all the different sets of data that you work with or have access to salesforce.
- Brainstorm what you could do with that data, what are the different applications.
- Based on that, what are the questions or things you'd want to learn?


# [15] How does the data science process work?
1. Data exploration
2. Data munging
3. Data modeling
4. Model evaluation
5. Model tuning
6. Productionize the model

Note: use Yipit deal categorization

# [5] What are the tools we'll be using
- Jupyter Notebook
- Python
- Pandas
- Scikitlearn
- Matplotlib
- Plotly

# [10] Intro to jupyter notebook 
# [10] Pandas demo
# [20] Pandas mechanics, exercises, practice, and debrief
# [20] TTL demo, exercise and debrief
# [15] Examining linked data
# [15] linked data demo, exercise and debrief
# [15] Explore the rock.csv dataset - any problems?


# [10] What is data munging? Why is it necessary?
- Why does ML depend so much on data?
- What happens if we have bad data?
- Discuss: examples of ML going haywire on bad data
- In what ways can data be bad?
- How much do companies spend on data munging? How can we resolve this for the future?

Note: Finhance data munging

# [10] Structured/unstructured data, different sources of data, databases
- What is structured data? Examples...
- What is unstructured data? Examples...
- What is a database?
- Relational databases vs noSQL databases - what's the relevance to you?

Note: Redis for recommendation data, not long-term persistent, quick retrieval


# [10] Explore the Boston housing dataset
# [10] What is statistics and why does it matter for us? How useful a tool is it?
- What is statistics?
- What's your relationship with statistics?
- To what extent does it matter? In what way?

# [10] What's the signifiance of mean, mode, variance, quartiles?
- Definitions
- What can we glean from these?
- Examples


Note: compensation calibration

# [10] Explore the stats and descriptive stats on this dataset... what do they mean?

# [10] Covariance, causation, correlation
- Spurious Correlations: http://tylervigen.com/spurious-correlations
- What is covariance? Why is this relevant for prediction?
- Causation vs correlation? Why is this distinction important?


# [10] What is modeling? 
- What is a model?
- Consider a model as a black box. What are its inputs and outputs?
- What are examples of models, in ML or not?
- Let's define what an ML model is...

Note: netflix movie recommendation, perceptron

# [10] High-level intro to supervised and unsupervised learning, probabilistic vs non-probabilistic models
- Supervised vs unsupervised
- How does supervised work? Need tagged data!
- Features vs target, training vs validation set
- Examples of supervised learning
- How does unsupervised learning work? Clustering...
- Examples of unsupervised learning
- *Bonus* Think about how you might use supervised and unsupervised learning together. Share.

# [10] What is probability, why does it matter and how does it work?
- Likelihood...
- Examples from your life

Note: churn analysis... one of my former students from Showtime, I believe

# [10] Probability mechanics and computation exercise
- Defining probability of an event (outcome over sample space) 
- Independent events
- Example problems

Note: use Venn diagrams for intuition

# [20] Conditional probability, intuition and math
- Suppose that A and B are not independent events.
- What does P(A|B) mean?
- What's the math?
- What's the intuition?
- Exercise: Out of 50 people surveyed in a study, 35 smoke in which there are 20 males. What is the probability the if the person surveyed is a smoker then he is a male? ([Source](http://www.probabilityformula.org/conditional-probability-examples.html))

Note: use Venn diagrams for intuition and to derive the formula, use the fun smile example for intuition

# [10] Explore setosa
- Play around with this and discuss with your neighbor http://setosa.io/conditional/
- Now let's share together what we learned

# [20] Model evaluation - how does that work?
- How should we evaluate whether a model is good or bad?
- What is good/bad?
- What is accuracy, precision and recall?
- What are some other limitations (X-fitting)

# [10] Different sources of error...
- error from variance
- error from bias

Look at this for visuals: http://scott.fortmann-roe.com/docs/BiasVariance.html

- Why does this matter?

# [10] Productionizing the model, reviewing results, testing hypotheses
- What does it mean to put a model in production?
- A/B testing
- The null hypothesis
- Was our modification significant?
- Brainstorm examples of A/B tests you would run at salesforce

Note: use Yipit subject line testing

# Open Q & A



