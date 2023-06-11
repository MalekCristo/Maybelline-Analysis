# Maybelline-Analysis

<img src="Maybelline-Emblem.png" width="250">

<H3 style="color:rgb(233, 99, 154);font-family:verdana;"> Outline and Objectives:</H3>

<u style="font-family:verdana;">This project aims to:</u>
<br>
<ol style="font-family:verdana;">
        <li> Explore and Analyze Maybelline's Product As a Whole.</li>
        <li> Analyze the Brand Image and Get an Overall Idea About Customers' Satisfaction using <b>Sentiment Analysis Tools.</b></li>
        <li> Use Sentiment Analysis Tools to Compare Maybelline With Other Competitors Sold On The Amazon Website.</li>
        <li> Identify Product Features That Customers are Searching for and Discussing using <b>Topic Modeling Techniques: LDA(Latent Dirichlet Allocation).</b></li>
</ol>


<H2  style="font-family:verdana;"> PART 1: Data Collecting & Web Scraping </H2>
<h3  style="font-family:verdana;"> <u>The use of Selenium as The Most Suitable Library</u></h3>

<p  style="font-family:verdana;"> We used Selenium as our web scraping library because we needed to interact dynamically with several websites: as scrolling down the page, signing up to amazon website, as well as clicking on next buttons etc...</p>
<p  style="font-family:verdana;">We identify these brands to scrape from data : </p>
<ul style="font-family:verdana;">
    <li>Sephora Collection</li>
    <li>Maybelline</li>
    <li>e.l.f</li>
    <li>Grande Cosmetics</li>
     <li>stila </li>
    <li>Kiss </li>
     
</ul>


<H2  style="font-family:verdana;"> PART 2: Data Cleaning & Preprocessing </H2>
<p> We performed data cleaning and preprocessing on numerical and text data.
        <br> Steps are detailed in the notebook.</p>
<H2  style="font-family:verdana;"> PART 3: Sentiment Analysis </H2>
<p>We choose the dictionary based sentiment analysis with the use of opinion dictionary. This method is easy to implement and has proven efficiency.
<br> 
We could classify reviews as positive, neutral, or negative.</p>

<H2  style="font-family:verdana;"> PART 4: Topic Modeling: LDA </H2>

<p>LDA is a widely used topic model in textual analysis. It supposes that a document is composed by a given
number of topics and each word in a document is linked to one of the document’s topics. <br> In our study,
the documents are represented by articles’ corpus. The term “latent” in LDA, as provided by the Oxford
Dictionary, signifies “existing, but not yet very noticeable, active, or well developed”. This indicates that
LDA topics are hidden topics and yet to be discovered by the model. This is a characteristic of the model
being an unsupervised machine learning technique first proposed by Blei (2003). In other words, the model is responsible to detect the heterogeneity in topics i.e. we are not required to specify lexicons
describing each topic as opposed to dictionary methods. LDA is based on the Dirichlet distribution which
is found in the 1800s by a German mathematician named Johann Peter Gustav Lejeune Dirichlet. In order
to generate these topics LDA assumes some rules:
<ul>
        <li> Articles dealing with the similar topics use similar words.</li>
        <li>Topics are identified as a group of words that are frequently employed together.</li>
        <li>Articles are a distribution over topics meaning that an article can contain more than one topic.</li>
</ul>
<br>
As an input, it takes the reviews’ text, the number of unique words appearing across all reviews, and the
number of topics that we are looking for. In our case, we ended up with 216080 documents.
<br>
LDA provides two outputs. As a first output, a set of K topics is generated as a probability distribution
of unique words, describing how frequently a word appears in a topic. The number of topics K is set
by the user depending on their needs and intuition. To do so, we examined the coherence scores, an
accuracy metric for LDA model, for different values of K. We could determine that a number of 7 topics
with an accuracy of Cv = 0.65 is the most suitable number for our case, i.e., the model’s results were the
most consistent and interpretable. Then it is our duty to label each topic based on the most frequent
words occurring in it. As a second output, LDA expresses each article as a probability-weighted average
of topics. The weights are called topic shares. These shares represent each topic’s contribution to a
review or the intensity of a topic’s appearance in a given review.
</p>
<H2> Limitations</H2>
<ul>
    <li> Be more inclusive about other competitors present on the same website. </li>
    <li> Use a more advanced algorithm in SA that treats better a large sample of data as CNN and LSTM.</li>
</ul>
