# How green is the media?

<p align="center" style="padding:10px;" >
  <img src="resources/newspaper_clipping_environment.jpg" alt="newspaper clipping environment"  />
</p>

Earth is experiencing a climate emergency as the climate is currently changing more rapidly than ever. In the scientific world, this has already been established but what about everyone else? The responsibility to communicate the causes, the consequences but also the means to limit global warming to normal people lies with the media. Our goal is to understand how the media has responded to this crisis by investigating the role of media sources when reporting speakers' opinion by analyzing their quotes. We will examine the quantity of quotes reported over time and their proportion compared to other topics to obtain an estimate of the relevance of the topic at hand. Moreover, we identify key characteristics of speakers in a given media source and compare these characteristics between different news sources. Opinions are shaped daily by the media and therefore we believe holding them accountable when it comes to urgent matters like this is essential.

For this study, we're conducting our analysis on the Quotebank dataset from the period of 2018-2020. Quotebank is a dataset of quotations from different newspapers and media sources, attributed to their speakers. This provides us with a rich dataset of quotations with different topics, from which we can filter the ones that talk about the environment, and upon which we can base our data story upon.


## Organization
1. Analysis of the most common profiles of the speakers who talk about the environment.
2. A time analysis of the topics 
3. Climate change representation in comparison with other topics.
4. Representation of topics in different newspapers 

## 1.  Would you talk about the environment?
The subject of the environment is brought to light by the people who talk about it. So if we're asking the question of whether the environment is well represented in the media, it stands to reason to know by whom is it usually represented.

In that sense, it's interesting to see who are the people that talk about the environment in the media and what are the characteristics that bring them together. In other words, what is **the common profile for the people that talk about the environment?**.


<p align="center" style="padding:20px;" >
  <img src="resources/unknown_speaker_profile.png" alt="unknown speaker profile"  />
</p>
 

 Note that this analysis was done **purely from the speaker's point of view**, we don't take into account in which newspaper or at what time period did the speaker utter this quotation. For this, we filtered the quotations that talk about the environment, and we retrieved their corresponding speakers along with their characteristics (or **features**). The initial method was easy enough, just count the features that appear most frequently within the environmental speakers. But that is not a sound idea, since the distribution of the features of the environmental speakers may be polluted by the underlying distribution of these features among all speakers.

 ![distribution of all speakers attributes](resources/distribution_of_speakers_attributes.png)

For instance, only 1% of all speakers are recorded having an academic degree. So if we count the ones who have spoken about the environment, we are bound to find that most them are uneducated because of the huge underlying overall distribution of the speakers without an academic degree. This can make us draw bad conclusions from this.

We need to come up with a better metric, that measures approximately the **likelihood of speaker talking about the environment based on a certain feature**. For this we can use the **ratio of environmental speakers per feature**. That is for a certain feature f we calculate:

*# environmental speakers with feature f / total # of speakers with feature f*

and we can translate this into the likelihood of speaker speaking about the environment, given he has feature f. 

We can now use this metric to compare the environmental ratios for the top occupations of the speakers, to the occupations with the highest said ratios:

![Environmental Ratios of top occupations vs Top environmental ratios](resources/occupation_top_ratios_vs_ratios_tops.png)

This tells us that you are more likely to talk about the environment if you were an American Football Player or a television actor than if you were a politician or a researcher!

<p align="center" style="padding:20px;" >
  <img src="resources/combining_speakers_features.svg" alt="Combining the ratios of the features together"  />
</p>

Now if we combine the top ratios from each feature separately, we get the following approximate environment speaker profile:
- They're likely working in **Arts & Entertainment**
- They're likely from the **LGBTQ community** (doesn't identify as *male* or *female*)
- They're likely from the **western hemisphere (culturally and politically speaking)**
- They're **older than 40 years old**
- They are **equally likely** to talk about the environment whether they **have an academic degree or not**.

 Note that up until now, we **isolated each feature** and then we did analysis on it separately from the other features. But one must remember that a speaker's profile is made up of several features, and sometimes the distribution of one feature may affect the distribution of another. And hence analysis should be made on the profile as a combined set of features, and not as a combination of analysis of each separate feature. 

## 2. Are we going in the right way?

If one is to tackle the problems introduced by climate change, one needs to be well informed. Such is the importance of an appropriate representation of environment related issues by the media. It is therefore of great interest and importance to analyse how such a portrayal has evolved over the years (in this particular case, from 2018 to 2020). 

We start our analysis by looking at the distribution of the number of articles (environment related) over the years.


<div style="text-align: center"><iframe src="resources/hist_all.html"></iframe></div>

At first hand, what strikes the most is the peak spanning from September 19, 2019 to September 28 of the same year. 
The sudden surge in articles for the aforementioned period could be explained by the fact that the Global Week for Future strikes (i.e. series of international strikes and protests to demand action be taken to address climate change) and the UN climate summit, took place at the same time.

As for the valleys, one could argue that another topic shifted media's attention during the given period. In particular, a possible explanation behind the low frequency of articles during the first months of 2020 could be the outbreak of COVID-19. Indeed, most media sources were mostly focused on keeping track with the evolution of the pandemic.

To add to this first analysis, we compute the average number of articles (environment related) per day:

| Year| Average number of articles (environment related) per day  |
| --- | --- |
| 2018 | 1106.693 |
| 2019 | 1348.170 |
| 2020 | 936.139 |

From 2018 to 2019, it appears there is an improvement in the media's awareness with respect to the environment. Unfortunately, this seems not to be the case for the following year. Does this mean that we're going backwards? Or is it just a temporary byproduct due to the unexpected events that took place over the year (events which could have stole the media's attention)? 

Now that we got an overall picture of the evolution (of the media's interest on the given topic) over time, it can be useful as well to do an analysis per media source case. For the later, we will focus on six media sources: MSN, Breitbart, Carbon Brief, CNN, N.Y. Times and Fox News. The following, is sequence of pie charts presenting the proportion that each of the media sources represents with respect to total number of environment related articles (for period of interest).


<div style="text-align: center"><iframe src="resources/pie_2018.html"></iframe></div>

<div style="text-align: center"><iframe src="resources/pie_2019.html"></iframe></div>

<div style="text-align: center"><iframe src="resources/pie_2020.html"></iframe></div>


N.B. It is advised to hide the "other news source" (from the pie chart), in order to get a better visual of the other proportions (i.e. the ones associated with the news sources of interest). This can be done by clicking on the name "other news source".

First of all, we can see that the proportions don't seem to vary that much over the years. What's more, among the articles from the news sources of interest (i.e. MSN, Breitbart, Carbonbrief, Fox News, N.Y. Times and CNN), almost half of them are from MSN. It is worth mentioning that the later is a news aggregator, which might explain the large number of articles. Mainstream media sources usually have a larger staff. Therefore, one could expect that said news sources would amount for the largest number of articles. However, this is not the case. Indeed, news sources such as Breitbart and Carbonbrief (which are "less" known), amount for more than a third of the articles from the news sources of interest (i.e. excluding "other news source"). Finally, we notice that the news sources studied only amount for around 3.2% of the total number of environment related articles.

## 3. Are we being fair ? A year in review. 

Is the environment equally represented in relation with other crucial topics? To answer this equation first we had to decide : Which other topics should we use in order to draw a meaningful comparison ? The topics we concluded to were LGBT Rights, Brexit and Gun Control. What lead us to this decision is our belief that during the time that our dataset is covering these topics were similarly occupying the common people and the press. Additionaly, they are all polarizing issues with multiple ethical standpoints but also potential devastating effects on the community. So, to answer this question we studied how these topics were represented during 2020.

To begin with, we noticed that in general the percentage of quotations related to the environment was less than 0.8% followed closely by LGBT rights while the other 2 topics were even lower. Moving on, we made an analysis as to how these topics are represented in newspapers. For this task we chose newspapers whose followers were considered to be either in liberal or conservative ideological group. Our conclusion was that the more conservative the readers of a certain newspaper were, the more the distribution of the quotes among those four topics was leaning towards the environment.

<p align="center" style="padding:20px;" >
  <img src="resources/topic_distribution.jpg" alt="unknown speaker profile"  />
</p>

 Next, we investigated this magnitude of environmental quotes but from a speaker's point of view. Our inquiry was the following : Given a group of people formed by a common attribute, in relation to the total amount of quotes made the same group of people, what percentage of these quotes was related to the environment ? Based on occupation our results the group of people with the highest numbers were the researchers, followed by the independent politicians and then the Germans.

<p align="center" style="padding:20px;" >
  <img src="resources/occupation_percentages.jpg" alt="unknown speaker profile"  />
</p>

Now coming back to our initial question, is the climate change sufficiently represented in the media? If only 1% of the quotations coming from politicians are about it do you think that that's enough to save the world? We believe that this question, is a question that every person should answer for himself.

## 4. Does it matter what you read?

To understand a bit more in depth which profiles of speakers are relevant when considerin specific news papers, we now focus on the top 10 news sources that we obtained by considering the entire environmental quotes between 2018 and 2020. We then specifically analyzed the following attributes 

- the speakers political party to see common profiles among news sources.
- their occupation which is often also linked to their political views.
- the age, which is especially interesting as more and more young people are present in social networks (think of Fridays for Future)

<p align="center" style="padding:20px;" >
  <img src="resources/distribution_top4_pol_parties.png" alt="unknown speaker profile"  />
</p>

We found that in particular people have been quoted with high shares by almost all news that belong to the Democratic Party and the Republican Party. What was striking was the rather high share of Democratic speakers that have been quoted by the right-winged news source *breitbart* (something unusual perhaps).
Also other parties are often represented such as the Autralian Labor Party, especially msn which is an online news source. The rather high frequency of quotes from people that are in the Democratic Party will also be the basis for our regression analysis.

<p align="center" style="padding:20px;" >
  <img src="resources/distribution_jobs_pernews.png" alt="unknown speaker profile"  />
</p>

Also their occupations differed quite a lot. Politicians, for example, were almost equally present in all news sources, higher for *einnews* and *smh*. Science-based news sources such as *eurekalert* and *phys* quoted researchers much more often than any other professions, something we would expect. Finally, we digged deeper for two rather opposing news sources: *breitbart*, a right-winged news magazine from the US (https://de.wikipedia.org/wiki/Breitbart_News_Network) vs *eurekalert* and tried to find out what features determine the likelihood with which someone is quoted about the environment by *breitbart*. We found that being in the Democratic Party dramatically increases (by a factor 2) ones chances while also the age plays an important role, although not as strong as expected. We also included the occupation, by encoding it as 1 of a speaker is either a researcher of journalist as these are jobs that are frequently under attack from people from the right spectrum. However, this feature did not turn out to be significant.


## Conclusion
In this study, we've tried to answer how the environment is represented in the media. It's a hard question to answer so we approached it from different angles: 
- It was interesting to see who's likely to speak about the environment 
- The time analysis shows a potential improvement in the media's portrayal of environment related topics (i.e. overall increase in the number of articles environment related over time). Unfortunately, said improvement came to a halt, presumably due to unprecented events which stole the media's attention (e.g. COVID-19 outbreak).
- On the one hand it is equally represented with other similar topics but on the other hand it is under-represented by politicians in comparison with the scientific community.
- 

We've seen that the environment is not equally represented across the media. 

A potential sentiment analysis on the quotes analysed could further complement the work done so far.

For a more detailed analysis you can visit our [original project Girhub page](https://github.com/epfl-ada/ada-2021-project-comic-sans).
