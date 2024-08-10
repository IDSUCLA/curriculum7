##**<u>Lesson 8: How Likely Is It?</u>**

###**Objective:**
Students will understand the basic rules of probability. They will learn that previous outcomes do not give
information about future outcomes if the events are independent.

###**Materials:**
1. Video: “Heads” from the movie *Rosencrantz and Guildenstern are Dead* found at:<br>
    [https://www.youtube.com/watch?v=NbInZ5oJ0bc](https://www.youtube.com/watch?v=NbInZ5oJ0bc "https://www.youtube.com/watch?v=NbInZ5oJ0bc"){:target="_blank"}

    <div align="right"><iframe width="420" height="315"
    src="https://www.youtube.com/embed/NbInZ5oJ0bc" allowfullscreen>
    </iframe><br><a href="https://www.youtube.com/embed/NbInZ5oJ0bc">https://www.youtube.com/embed/NbInZ5oJ0bc</a></div>

2. Projector for RStudio functions

###**Vocabulary:**
[probability](../../vocabulary/unit2/#probability "how likely it is that some event will occur"){ .md-button }
[simulation](../../vocabulary/unit2/#simulation "a way of creating random events that are close to real-life situations without actually doing them"){ .md-button }
[model](../../vocabulary/unit2/#model "a way of representing real world situations so that predictions can be made"){ .md-button }
[sample proportion](../../vocabulary/unit2/#sample-proportion "the fraction of samples which were successes"){ .md-button }
[chance](../../vocabulary/unit2/#chance "the possibility that something will happen"){ .md-button }
[independence](../../vocabulary/unit2/#independence "if one event doesn't affect the outcome of another event"){ .md-button }

###**Essential Concepts:**

!!! note "Essential Concepts: "
    Probability is an area about which we humans have poor intuition. Probability
    measures a long-run proportion: 50% chance means the event happens 50% of the time *if you repeated it
    forever*. When we don't repeat forever, we see variability.

###**Lesson:**

1. Ask students to consider possible synonyms for the word **chance**. If someone says, “That just
happened by chance,” what does that mean? <span style="color:grey">***Synonyms: possibility, prospect, expectation,
unintentional, unplanned. The actual definition of chance is “a possibility of something
happening.”***</span>

2. Then, ask them which game – chess or the board game, “Sorry” – is more based on chance. Why?  
 **<u>Note:</u>** Any game can be
chosen. <span style="color:grey">***"Sorry" is more based on chance because many
outcomes are determined by dice rolls. In chess there are certain strategies and
movements that can be planned, so it is more a game of skill. For "Sorry" the players roll a
die (number cube), so the numbers they roll have an impact on how well they do in the
game.***</span>

3. Next ask students if they can think of situations where chance is the only force at play. <span style="color:grey">***Possible
responses: card games, slot machines, the lottery, coin flipping, and rock-paper-scissors.***</span>

4. Play the “Heads” video from the movie *Rosencrantz and Guildenstern are Dead* found at:
[https://www.youtube.com/watch?v=NbInZ5oJ0bc](https://www.youtube.com/watch?v=NbInZ5oJ0bc "https://www.youtube.com/watch?v=NbInZ5oJ0bc"){:target="_blank"}.

5. In their IDS Journals, ask students to write down their initial reactions to the clip by responding to
the following questions:

    100. Is it *possible* to get 78 heads in a row when tossing a coin? <span style="color:grey">***Answer: Yes, it is possible to get 78
    heads in a row since one coin toss does not determine the next coin toss.***</span>

    100. Do you think it is *likely* to get 78 heads in a row? <span style="color:grey">***Answer: No, although it is possible to get 78
    heads in a row.***</span>

    100. How many times should we get heads when tossing a coin? <span style="color:grey">***Answer: 1 out of 2 times, or 50% of
    the time.***</span>

    100. On average, how many times out of the 78 tosses should the characters have gotten heads? <span style="color:grey">***Answer: Roughly 39 times.***</span>

6. Ask students to discuss their findings with their team members and come to an agreement on
their responses. Afterwards, conduct a *Whip Around* and ask each team to share its findings. Are
there any differences between the teams? Any similarities?

7. As teams share their responses, students should add to or revise their individual findings in their
IDS Journals.

8. Explain to students that, from the concept of chance, we can start learning about **probability**.
Chance is simply the possibility that something will happen, and probability is a measurement for
how often something happens in the “long run.” Students may have ideas about how to calculate
probabilities based on prior classes or knowledge, but inform them that IDS will be taking a
different approach by using simulations (see next step).

9. Since we don’t want to actually flip a coin 78 times like the actors did in the video, we can have
RStudio simulate them for us. A **simulation** is a way of creating random events that are close to
real-life situations without actually doing them. It is a kind of **model**, which is a way of
representing real-world situations so that predictions can be made.

10. Explain to students that R has a function that does coin flipping for us, and that it assumes an
equal probability of heads and tails. Using a projector to display your computer screen to the
whole class, demonstrate how to do one simulation of a coin flip in RStudio. Use the following
function:

    **> rflip(1)**

11. Explain that the value of 1 in the argument part of the function tells R to flip the coin 1 time. If we
want to flip the coin 10 times, we could simply change the function to ```rflip(10)```.

12. Run the function again using 10 as the number of times to flip the coin. Ask students:

    100. How many heads (“H”s) were there? <span style="color:grey">***Answers will vary for each sample.***</span>

    100. How many Tails (“T”s) were there? <span style="color:grey">***Answers will vary for each sample.***</span>

    100. In the output, what does **Flipping 10 coins [Prob(Heads) = 0.5]** mean? <span style="color:grey">***Answer: This is
    RStudio telling us that we are tossing the coin 10 times and that the***</span> **probability** <span style="color:grey">***of
    getting heads is 0.5 because it is a fair coin.***</span>

    100. In the output, what does **Number of Heads: 3 [Proportion Heads: 0.3]** mean? <span style="color:grey">***Answer: This is RStudio telling us that in our sample, we got heads 3 out of the 10 times we flipped the coin. The***</span> **sample proportion** <span style="color:grey">***is automatically calculated for us by dividing the number of heads by the total number of tosses (in this case, 3/10=0.3).***</span>
    
        **<u>Note:</u>** This is an example of an output. Your sample may have a different value for the number of
        heads that appeared, and therefore a different value for the proportion of heads.

13. To relate back to the video at the beginning of class, repeat the simulation once more, but use 78
as the number of coin flips ```rflip(78)```. Ask students:

    100. How many heads (“H”s) were there? Since we know to expect about 39 heads if the coin
    is fair, does the value seem reasonable? <span style="color:grey">***Answers will vary for each sample. Most
    likely, you will see values near 39.***</span>

    100. How many Tails (“T”s) were there? <span style="color:grey">***Answers will vary for each sample.***</span>

    100. What proportion of the coin flips were heads? <span style="color:grey">***Answers will vary for each sample.***</span>

14. Using the **rflip(78)** command, run the simulation 3-5 more times and have students
record the values for the number of heads and the proportion of heads.

    <span style="color:grey">***As an example, we ran the function 3 times and saw the following values:***</span>

    <span style="color:grey">***Sample 1 – amount of heads: 45***</span>

    <span style="color:grey">***&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;proportion of heads: 0.577***</span>

    <span style="color:grey">***Sample 2 – amount of heads: 33***</span>

    <span style="color:grey">***&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;proportion of heads: 0.423***</span>

    <span style="color:grey">***Sample 3 – amount of heads: 42***</span>

    <span style="color:grey">***&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;proportion of heads: 0.538***</span>

15. Have students answer the questions below. The important thing to note is that the values
can and (almost always) WILL change each time you run the simulation to create a new sample.

    100. How do the proportions of heads in the samples compare to each other? <span style="color:grey">***Answers will
    vary.***</span>

    100. How do the proportions of heads compare to the true probability of heads (1/2 or 50%)?
    <span style="color:grey">***Answers will vary, but students should notice that most of the probabilities are close to
    50%.***</span>

    100. Why is there a 50% chance of getting heads during each coin flip? <span style="color:grey">***Answer: Since there are two
    sides to a coin, both should be equally likely to come up. So there is a 1 out of 2
    chance of getting heads and 1 out of 2 chance of getting tails.***</span>

16. Ask students to engage in a discussion with their group about the statement below, then have a few group reporters share out.

    100. If a coin was flipped 78 times, I would claim that the coin is unfair if I got less than <b><span style="color:purple">#</span></b> heads or more than <b><span style="color:purple">#</span></b> heads.

17. Inform students that you are going to perform 500 simulations. Each simulation represents a coin being flipped 78 times. For each simulation, the computer will record the number of heads in the 78 flips. A histogram will be created that represents the number of heads in each of the simulations. The histogram is a model that will display what typically happens when a fair coin is flipped 78 times.

18. Copy and paste the code below in an RScript and run each line of code, one at a time, for the students:


        set.seed(11) #reproducibility 
        flips <- do(500)*rflip(78)  
        View(flips) # 4 variables
        histogram(~heads, data = flips)  
        favstats(~heads, data = flips)

19. Engage the students in a discussion about the histogram:

    100. What is this distribution telling us?
    <span style="color:grey">***Answer: When flipping a fair coin 78 times, what typically happened was that it landed on heads between 36 and 42 times (36/78 = 0.46 to 42/78 = 0.54). It was not uncommon for the coin to land on heads 28-35 (0.36-0.45) times or 43-51 (0.55-0.65) times. What was very uncommon, however, was landing on heads less than 28 times (less than 36%) or more than 51 times (more than 65%).***</span>

    100. Were your group's cut-offs (item #16) similar to what the chance model displayed?
    <span style="color:grey">***Answers will vary. Some groups' intervals might be very wide and others very narrow.***</span>

    100. Using the chance model (histogram) which displays what typically happens when a fair coin is flipped 78 times, make a call for the scenarios below - fair or unfair?

        100. You flip a coin 78 times and get 37 heads.
        <span style="color:grey">***Answer: Fair. 37 was very common based on the histogram.***</span>
        
        100. You flip a coin 78 times and get 46 heads.
        <span style="color:grey">***Answer: Fair. 46 was less common but not too uncommon.***</span>
        
        100. You flip a coin 78 times and get 20 heads.
        <span style="color:grey">***Answer: Unfair. In the 500 simulations not once did we see a FAIR coin land on heads 20 times. ***</span>

20. Next pose the following question:

    100. If you get a heads on the first toss of a coin, will you definitely get a heads on the next
    toss? Will you definitely get a tails on the next toss? <span style="color:grey">***Answer: No. One coin toss should not
    affect another coin toss. Each time you flip the coin, the chances of getting heads
    versus tails remains the same.***</span>

21. Introduce the concept of **independence**. Explain that, when tossing a fair coin, there is no
relationship between each toss. The second toss does NOT depend on the first toss; therefore,
the coin tosses are independent of each other.

###**Class Scribes:**
One team of students will give a brief talk to discuss what they think the 3 most important topics of the
day were.

###<p style="background: black; color: white; text-align: center;">**Homework**</p>
Students will create a Tweet (they do not have to post it online). Using 280 characters or fewer, write a
Tweet about the meaning of probability.