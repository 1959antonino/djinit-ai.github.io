---
layout:     post
title:      Apriori Algorithm
date:       2020-09-22 07:40:40
summary:    Implementations of Apriori Algorithm
categories: Python, Association Rule Learning
---

<h1>Apriori Algorithm</h1>

Ever wondered how predicting the future at every stage of our lives will make our lives so convenient? Because what we don’t realise is, our life is filled with patterns.
Won’t it be great to analyse these already existing patterns to make our lives easier? Well, don’t worry, Data Mining has got you covered. Data mining is the exploration and analysis of large data to discover meaningful patterns and rules.
<br>
<p align="center">
<img src="/images/Apriori-Algorithm-1.png" height=300 width=400 />
</p>

There are various types of Data Mining techniques available. The one which seems to be the most naive yet powerful is Apriori Algorithm.<br>
a priori;  a Latin word, literally means ‘from what is before’. Hence Apriori Algorithm is an efficient way of Data Mining where the most frequent itemsets and association rules for a transactional database can be identified. Wait, did that confuse you? Don’t worry because that's why we are here.<br>
Let’s take one step at a time.<br>
<br>
<h2>What are Association Rules?</h2>
The rules devised during the process of Associate Rule Mining (ARM) are called Associate Rules.
Being an integral part of Data Mining, ARM helps us create simple IF/THEN rules statements that help discover relationships and patterns between items in the database, and to consequently predict the next item set.  The biggest application of ARM in today’s world is business decisions and analytics.
<br>
In layman's language, it is the creation of rules such as IF a customer purchases a product A THEN the customer is also likely to purchase product B.
In technical terms, such a product A is called an Antecedent (IF), and product B an Consequent (THEN).
<br>
But if determining such a IF/THEN relationship was so simple, why would we need the Apriori Algorithm? The answer lies in the fact that for a single product A, there are probably 9999 such products B, which hold some sort of resemblance. Apriori aims to solve this exact problem.
<br>
<h2>The Algorithm Explained</h2>
Apriori algorithm uses frequent itemsets to generate association rules. It is based on the concept that a subset of a frequent itemset must also be a frequent itemset. Items in a transaction form an item set. The algorithm proceeds to find frequent itemsets in the database and continues to extend them until it reaches the threshold. Frequent Itemset is an itemset whose support value is greater than a threshold value.
<br>
The apriori algorithm uses the downward closure property ,i.e., all the subsets of a frequent itemset are frequent, but the converse may not be true.

<p align="center">
<img src="/images/Apriori-Algorithm-2.png" height=350 width=400 />
</p>
But this was just the intuition, how do things actually work?
Let’s dive into the mathematics of the algorithm, and for which we will need to know 3 important terms
<br>
<ol>
  <li>Support</li>
  <li>Confidence</li>
  <li>Lift</li>
</ol>

<h3>Support:</h3>
Support basically refers to the number of times the chosen item/s appears in the database, i.e the frequency of the item/s. Having said this, it is quite easy to guess it’s formula,
<br>
<p align="center">
<img src="/images/Apriori-Algorithm-3.png" height=50 width=200 />
</p>
<br>
Where freq(A,B) denotes the frequency of A and B appearing together in a transaction, and N denotes the total number of items in the database.
<h3>Confidence:</h3>
Remember the concept of Conditional Probability from highschool? Let’s revise it again.<br>
Conditional Probability refers to a special type of probability where an event will occur, <b>given</b> a particular event has already happened. This is exactly what confidence is. In other words, Confidence refers to the frequency of A and B being together, given the number of times A has occurred.
<br>
<p align="center">
<img src="/images/Apriori-Algorithm-4.png" height=50 width=200 />
</p>
<h3>Lift:</h3>
The lift of a rule is defined as:
<br>
<p align="center">
<img src="/images/Apriori-Algorithm-5.png" height=50 width=200 />
</p>
<br>
This signifies the likelihood of the itemset B being purchased when item A is purchased while taking into account the support of B
<br>
The main steps involved in the algorithm are:
<br>
<ol>
    <li>Calculate the support (frequency) of item sets (of size K = 1) in the transactional database. This is called generating the candidate set.</li>
    <li>Prune the candidate set by eliminating items with a support less than the given threshold. Pruning basically means eliminating the itemsets which are not necessary, hence refining the itemsets.</li>
    <li>Join the frequent itemsets to form sets of size k + 1, and repeat the above sets until no more itemsets can be formed. This will happen when the set(s) formed have a support less than the given support.</li>
</ol>
<br><br>
<p align="center">
<img src="/images/Apriori-Algorithm-6.png" height=300 width=580 />
</p>
<br>
That was a lot of theory! Let’s now have a look at the most popular use case of the Apriori Algorithm, Market Basket Analysis.
<br>
<h2>Market Basket Analysis</h2>
<br>
The approach is based on the hypothesis that customers who buy a certain item (or group of items) are more likely to buy another specific item (or group of items).
<br>
Wait, is it just me, or does this sound very much similar to Apriori? Infact, Market Basket Analysis is entirely based on the Apriori algorithm itself.
The relations hence can be used to increase profitability through cross-selling,
recommendations, promotions, or even the placement of items on a menu or in a store.
<br>
<p align="center">
<img src="/images/Apriori-Algorithm-7.png" height=350 width=850 />
</p>
<br>
<h2>Understanding our used case:</h2>
For the implementation of Apriori algorithm, we are using data collected from a SuperMarket, where each row indicates all the items purchased in a particular transaction.
<br>
The dataset has 7,500 entries .
The link to the dataset -
<br>
https://drive.google.com/file/d/1nGzgX2cq8R4AT-9cMq_puzB1XgPnb6Pf/view?usp=sharing
<br><br>
<p align="center">
<img src="/images/Apriori-Algorithm-8.png" height=500 width=850 />
</p>
<br>
<h2>Python Implementation</h2>
<b>STEP 1:</b>  Let’s install the apyori module.
<br>
Apyori is a simple implementation of Apriori algorithm with Python 2.7 and 3.3 - 3.5, provided as APIs and as command-line interfaces.
<br><br>
<p align="center">
<img src="/images/Apriori-Algorithm-9.png" height=60 width=400 />
</p>
<br>
<b>STEP 2:</b>  We import the necessary libraries required for the implementation.
<br><br>
<p align="center">
<img src="/images/Apriori-Algorithm-10.png" height=90 width=500 />
</p>
<br>
<b>STEP 3:</b> Reading the dataset
<br>
Now we have to proceed by reading the dataset we have , that is in a .csv format. We do that using pandas module’s read_csv function.
<br>
The apyori module’s apriori function takes primary input in a list format. For this purpose, we first create an empty list named ‘transactions’.
<br>
Iterating through all our rows, i.e. 7500 entries, we append each of the values of the row after converting all the inputs into a string.
<br>
The inner loop is of range(0,20) , as we have maximum 20 values in a particular row entry. For other rows having less than 20 values, we automatically consider the remaining as null inputs.
<br><br>
<p align="center">
<img src="/images/Apriori-Algorithm-11.png" height=110 width=800 />
</p>
<br>
<b>STEP 4:</b> We import the apriori function from the apyori module. We store the resulting output from apriori function in the ‘rules’ variable.
<br>
To the apriori function, we pass 6 parameters:
<ol>
    <li>The transactions List as the main inputs</li>
    <li>Minimum support, which we set as 0.003
    We get that value by considering that a product should appear at least in 3 transactions in a day. Our data is collected over a week. Hence , support value should be 3*7/7500 = 0.0028</li>
    <li>Minimum confidence, which we choose to be 0.2 (obtained over analyzing various results)</li>
    <li>Minimum lift, which we’ve set to 3</li>
    <li>Minimum Length is set to 2, as we are calculating the lift values for buying an item B given another item A is bought, so we take 2 items into consideration.</li>
    <li>Minimum Length is set to 2 using the same logic.</li>
</ol>
<p align="center">
<img src="/images/Apriori-Algorithm-12.png" height=80 width=950 />
</p>
<br>
<b>STEP 5:</b> We print out the results as a List
<br><br>
<p align="center">
<img src="/images/Apriori-Algorithm-13.png" height=300 width=950 />
</p>
<br>
<b>STEP 6:</b> Visualizing the results
<br>
In the <b>LHS</b> variable, we store the first item from all the results, from which we obtain the second item that is bought after that item is already bought, which is now stored in the <b>RHS</b> variable.
<br>
The <b>supports, confidences and lifts</b> store all the support, confidence and lift values from the results.
<br><br>
<p align="center">
<img src="/images/Apriori-Algorithm-14.png" height=250 width=950 />
</p>
<br>
Finally, we store these variables into one dataframe, so that they are easier to visualize.
<br><br>
<p align="center">
<img src="/images/Apriori-Algorithm-15.png" height=500 width=850 />
</p>
<br>
<b>Now</b>, we sort these final outputs in the descending order of lifts.
<br><br>
<p align="center">
<img src="/images/Apriori-Algorithm-16.png" height=500 width=850 />
</p>
<br>
This is the final result of our apriori implementation in python. The SuperMarket will use this data to boost their sales and prioritize giving offers on the pair of items with greater Lift values.
<br>
<h3>Why Apriori?</h3>
<ol>
    <li>It is an easy-to-implement and easy-to-understand algorithm.</li>
    <li>It can be easily implemented on large datasets.</li>
</ol>
<h3>Limitation of Apriori algorithm</h3>
Frequent Itemset Generation is the most computationally expensive step because the algorithm scans the database too many times, which reduces the overall performance. Due to this, the algorithm assumes that the database is Permanent in the memory.
<br>
Also, both the time and space complexity of this algorithm are very high: O(2^{|D|}), thus exponential, where |D| is the horizontal width (the total number of items) present in the database.
<h3>A common mistake</h3>
Association involves analysing the underlying patterns in the given transactions in all possible ways, whereas
<br>
Recommendation is the process of predicting the possible outcome based on the individual transaction history of the consumer.
<br>
To understand it better, take a look at the snapshot below from amazon.in and flipkart.in and you will notice 2 headings “Bought Together” and the “Customers who viewed this item also viewed” on each product’s information page.
<br><br>
<p align="center">
<img src="/images/Apriori-Algorithm-17.png" height=300 width=850 />
</p>
<br><br>
<p align="center">
<img src="/images/Apriori-Algorithm-18.png" height=300 width=850 />
</p>
<br>
<i>Bought Together</i> shows the associative results.
<br>
<i>Customers who viewed this item also viewed</i> gives us the recommendations.
<br>
<h3>Summary</h3>
<br>
<p align="center">
<img src="/images/Apriori-Algorithm-19.png" height=120 width=650 />
</p>
<br>
Apriori Algorithm is an unsupervised learning technique which aims at associating items from a transactional database to give us rules which will predict the buying/occurrence patterns. The flowchart above will help summarise the entire working of the algorithm.
<br>
