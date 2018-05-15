Are Movies Getting Better?
--------------------------

Our analysis focussed on lists of movies from Rotten Tomatoes giving the
top 100 movies in any given year. We took the most recent 20 of these
lists with their critic scores and number of reviews in order to ask the
following questions: Have the scores of movies increased over time? If
so, why? Does the number of reviews come into play? Audience score? how
do movies with a 100% critic score fare in other categories?  
Our goal in this analysis is not to difinitvely answer if movies have
gotten better, but to see if there is statistical backing to the trend
of recent movies getting high scores. Are the critics giving higher
scores? Are audiences getting more involved in scoring online?  
Are movies getting better?

![](Index_files/figure-markdown_strict/Critic%20Score%20Plots-1.png)

Our preliminary graph shows that the average score of films has gone up
over the past 20 years. This line graph is simply the average score per
year, connected to show the basic trend. The points show each individual
score, with a slight jitter added for visibility.  
Next, we have the distribution of critic scores, where we can see the
majority of films lie between 80 and 100. The movies below 80 tend to be
from before 2010, with the lowest score in 1998.  
The density plot below shows similar information, but with lines and
clearer data.

![](Index_files/figure-markdown_strict/graphs%20with%20words%20beforehand-1.png)![](Index_files/figure-markdown_strict/graphs%20with%20words%20beforehand-2.png)

![](Index_files/figure-markdown_strict/Reviewer%20Plots-1.png)![](Index_files/figure-markdown_strict/Reviewer%20Plots-2.png)

The average number of reviewers also goes up over time. What is
interesting about this data is that we don't see a spike in the data at
any point. Rotten Tomatoes was launched in August of 1998 and has only
grown since then, and our data does reflect that throught the increase
in review numbers. The increase is not as large as one may expect, with
Rotten Tomatoes being a go-to review site. This suggests that perhaps
the number of reviews depends on the movie itself more than when the
movie was released. Or, that Rotten Tomatoes has gained popularity and
notariety, but has not grown in its reveiwer numbers. Either way, the
number of reviewers does not seem to have an impact in scores, and does
not determine which movies are in the top 100 for each year.

![](Index_files/figure-markdown_strict/Comparing%20plots-1.png)![](Index_files/figure-markdown_strict/Comparing%20plots-2.png)

This list is a tibble of movies that recieved a 100% from critics by
year. This list shows how 2017 and 2016 have had more 100% ratings than
any other year. It furthers our point of average scores increasing,
based on the fact that these movies are all recent rather than from
1998.

    ## # A tibble: 34 x 4
    ##    Title                                            Score Review_num Year 
    ##    <chr>                                            <dbl>      <dbl> <chr>
    ##  1 Quest (2017                                        100       53.0 2017 
    ##  2 Bright Lights: Starring Carrie Fisher and Debbi…   100       53.0 2017 
    ##  3 The Work (2017                                     100       52.0 2017 
    ##  4 The Happiest Day in the Life of Olli Mäki (Hymy…   100       49.0 2017 
    ##  5 Dawson City: Frozen Time (2017                     100       45.0 2017 
    ##  6 Dolores (2017                                      100       41.0 2017 
    ##  7 Things to Come (L'avenir) (2016                    100      130   2016 
    ##  8 Tower (2016                                        100       78.0 2016 
    ##  9 O.J.: Made in America (2016                        100       50.0 2016 
    ## 10 The Age of Shadows (2016                           100       41.0 2016 
    ## 11 Fireworks Wednesday (Chaharshanbe-soori) (2016     100       41.0 2016 
    ## 12 GETT: The Trial of Viviane Amsalem (2015           100       73.0 2015 
    ## 13 Seymour: An Introduction (2015                     100       63.0 2015 
    ## 14 Court (2015                                        100       46.0 2015 
    ## 15 3 And 1/2 Minutes, 10 Bullets (2015                100       45.0 2015 
    ## 16 The Tale of the Princess Kaguya (2014              100       85.0 2014 
    ## 17 Ilo Ilo (2014                                      100       42.0 2014 
    ## 18 The Square (Al Midan) (2013                        100       61.0 2013 
    ## 19 Sound City (2013                                   100       44.0 2013 
    ## 20 Wake in Fright (2012                               100       51.0 2012 
    ## 21 Poetry (2011                                       100       64.0 2011 
    ## 22 Everyday Sunshine: The Story of Fishbone (2011     100       45.0 2011 
    ## 23 We Were Here (2011                                 100       43.0 2011 
    ## 24 Nostalgia for the Light (2011                      100       43.0 2011 
    ## 25 Waste Land (2010                                   100       69.0 2010 
    ## 26 Last Train Home (2010                              100       54.0 2010 
    ## 27 Afghan Star (2009                                  100       60.0 2009 
    ## 28 Man on Wire (2008                                  100      157   2008 
    ## 29 Aruitemo Aruitemo (Still Walking) (2008            100       62.0 2008 
    ## 30 Taxi to the Dark Side (2007                        100       93.0 2007 
    ## 31 Deliver Us from Evil (2006                         100       73.0 2006 
    ## 32 Le goût des autres (The Taste of Others) (2000     100       58.0 2000 
    ## 33 Toy Story 2 (1999                                  100      163   1999 
    ## 34 Mr. Death: The Rise and Fall of Fred A. Leuchte…   100       39.0 1999

The plots below compare a select group of movies' critic scores to their
audience scores. To get the audience scores, we had to look ta each
movie's page individually, so we only did the top 20 movies 2017, 2008,
and 1998. Critics scores were cosistently higher than audience scores,
and audiences even had outliers that were extremely low in 1998 and 2017
(Antz and Star Wars). The box plot shows the lower scores as outliers in
better detail. They are far lower than the lowest critic score. This
tells us that audience score is not a large factor in how great the
movies are, as both Antz and Star Wars are in the top ten of their
respective years. This discrepancy was a surprise, but we suspect that
audience scores are brought down by people being more opinionated; only
giving very high or very low reviews.  
The tibbles document rare cases where the audience score matched the
critic score and cases where the audience score was higher than the
critic score. Between these two parameter sets, there are only five
films, and all of the films with higher audience scores are from 1998.
The rarity of such cases further shows how critics scores increase over
time.

![](Index_files/figure-markdown_strict/Audience%20vs%20Critics-1.png)![](Index_files/figure-markdown_strict/Audience%20vs%20Critics-2.png)

    ## # A tibble: 2 x 5
    ##   Title             `Critic Score` `Critic Reviews`  Year `Audience Score`
    ##   <chr>                      <dbl>            <dbl> <dbl>            <dbl>
    ## 1 Hidden Figures (…           93.0              262  2017             93.0
    ## 2 The Dark Knight …           94.0              327  2008             94.0

![Hidden
Figures](~/Mscs%20264%20S18/Inclass/Schrader_Voegele/__59dd139766efd.jpg)
![The Dark
Knight](~/Mscs%20264%20S18/Inclass/Schrader_Voegele/13349231_f520.jpg)

    ## # A tibble: 3 x 5
    ##   Title             `Critic Score` `Critic Reviews`  Year `Audience Score`
    ##   <chr>                      <dbl>            <dbl> <dbl>            <dbl>
    ## 1 Saving Private R…           92.0            132    1998             95.0
    ## 2 Central Station …           94.0             48.0  1998             95.0
    ## 3 Rushmore (1998              89.0            102    1998             91.0

Based on our data and graphical evidence, we see how over the past 20
years, average critic scores of films have gotten higher, while audience
scores, despite growning in numbers, have consistently had lower scores
than the critics. Does this mean that critics are going easy on newer
films? Are audiences becoming more critical? Or are movies truly getting
better? We may not know the exact reasons behind this trend, but it will
be interesting to see how scores change. Our prediction is that average
scores will plateau in the 90% range over the next few years.
