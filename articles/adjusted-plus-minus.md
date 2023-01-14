---
layout: default_math 
--- 

We conduct a literature review of the adjusted plus-minus metric in sports. 

https://simplystatistics.org/posts/2021-11-10-thinking-about-failure-in-data-analysis/
> In both success and failure it is valuable to consider the unobserved outcomes in the potential outcome set and ask whether we should be observing one of those other outcomes, perhaps because there exists a better model or because the data should be processed in a different way. It is this consideration of the potential outcomes of an analysis, as well as the alternating between success and failure, that drives the iterative nature of data analysis. Ultimately, we want to come to a place where we feel we understand the data, the data generation process, and the analytic process that leads to our result.

* [] We might want to take an exerpt of this quote rather than the whole thing. 


Exercise: What are the weaknesses of the plus-minus metric? 

Exercise: Set up a regression model to adjust the 

Exercise: What are the weaknesses of the adjusted plus-minus metric? 
* It lumps together players' contribution to offense and defense. It is possible that a player is good offensively but horrible defensively. In that case, their contribution could average out to zero. What we would like is to detect this so that we can have the player play offensively but not defensively. Ilardi and Barzilai model these separately. 

Exercise: What is the consequence of large standard errors for the regression coefficients? 
* "To take a telling example: Chris Paul had a 2006-2007 rating of +4.1 pts (per 40 minutes), with a margin of error of roughly +/- 5.9; so, we can only say with 95% confidence that his performance was somewhere between that of a sub-mediocre player (-1.8) and one of the top players in the league (+10.0)!" (Ilardi and Barzilai) 
* If features are correlated, the 

A comprehensive review of plus-minus ratings for evaluating individual players in team sports, International Journal of Computer Science in Sports, Hvattum, 2019

"comparing the performance of the team with and without the player" 

"basic plus-minus ratings ignore the quality of a player's teammates and opponents. The consequence is that poor players on good teams are overrated, while good players on poor teams are underrated." 



Adjusted Plus-Minus Ratings: New and Improved for 2007-2008, Steve Ilardi and Aaron Barzilai

"disentangle the individual effects of teammates who frequently appear on the court at the same time" 

"In addition, we've modeled separately each player's impact on offense and defense, treating these components as independent variables" 


A Review of Adjusted Plus/Minus and Stabilization, Daniel Myers, 2011 

"some players have a very small sample size, so they may muddy the final results by basically taking up all of the residual in the few minutes they played. Many APM approaches ... lump the rarely-used players into an 'other players' bucket and just average them out. This should improve the estimates on the players that are actually rated." 
