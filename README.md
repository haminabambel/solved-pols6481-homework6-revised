Download Link: https://assignmentchef.com/product/solved-pols6481-homework6-revised
<br>
Download the dataset <em>SLEEP75.DTA</em> which contains individual-level data collected for a study on <strong><em>sleep</em></strong>, which is the dependent variable, measured as the average number of <u>minutes</u> per week.

Run the following line of code to limit your study to the 515 married adults in the sample:

&gt; sleep &lt;- read.dta(“C:/Users/Scott/SLEEP75.DTA”)

&gt; married &lt;- subset(sleep, yrsmarr &gt; 0)

Recall that in Homework Assignment 5, you estimated the following regression model using ordinary least squares:

where <strong><em>totwrk</em></strong> is average minutes worked per week, from 0 (unemployed) to 6415 (100+ hours);

<strong><em>age</em></strong> measures the respondent’s age;

<strong><em>agesq</em></strong> equals age<sup>2</sup>.

Now our attention is on three new variables:

<strong><em>female</em></strong> indicates whether the respondent is a woman;

<strong><em>yngkid</em></strong> indicates whether there is a child under 3-years-old in the house;

<strong><em>interaction</em></strong> is the product of <strong><em>female</em>*<em>yngkid</em></strong>;

<ol>

 <li>Run the following two lines of code to create the female variable and the interaction term …</li>

</ol>

&gt; married$female = 1-married$male

&gt; married$interaction = married$female*married$yngkid

… then run a linear regression model with these six independent variables, and report your results:

<ol start="2">

 <li>Use your results from 1. to answer some additional questions about interaction terms involving two binary (qualitative) variables, female and yngkid.</li>

</ol>

<ol>

 <li>What is the marginal effect of having a young kid on sleep? State it first as a literal equation, and then substitute numeric values based on the regression model.</li>

</ol>

=

=

<ol>

 <li>What is the standard error of the marginal effect of having a young kid on sleep? Again, state it first as a literal equation, and then substitute numeric values from the regression model’s variance-covariance matrix of the estimators.</li>

</ol>

s.e.() =

=

<ol>

 <li>What is the marginal effect of gender on sleep? State it first as a literal equation, and then substitute numeric values based on the regression model.</li>

</ol>

=

=

<ol>

 <li>What is the standard error of the marginal effect of gender on sleep? Again, state it first as a literal equation, and then substitute numeric values from the regression model’s variance-covariance matrix of the estimators.</li>

</ol>

s.e.() =

=

<ol>

 <li>Set <strong><em>age</em></strong> = 35, set <strong><em>agesq</em></strong> = 1225, and set <strong><em>totwrk</em></strong> = 2112; calculate the predicted sleep per week for…</li>

</ol>

(i) a male without a young child                 <u>                </u> minutes

(ii) a male with a young child                       <u>                </u> minutes

(iii) a female without a young child           <u>                </u> minutes

(iv) a female with a young child                  <u>                </u> minutes

<ol>

 <li>For a <u>man</u>, how does having a young child impact sleep? Use the values in e. to calculate the difference in predicted sleep.</li>

 <li>Is this effect statistically significant? Use your answer to b. to calculate the standard error of the marginal effect and <em>t </em>statistic.</li>

 <li>For a <u>woman</u>, how does having a young child impact sleep? Use the values in e. to calculate the difference in predicted sleep.</li>

 <li>Is this effect statistically significant? Use your answer to b. to calculate the standard error of the marginal effect and <em>t </em>statistic.</li>

 <li>Check your answers to g. and i. using the trick I taught in class, changing the baseline group from males to females. You will need to replace the variable female with the variable male and run the following line of code to create an interaction between male and yngkid:</li>

</ol>

&gt; married$interaction_m = married$male*married$yngkid







Download the dataset <em>TradeConflictK12.dta</em> which contains dyadic data collected for a study on <strong><em>trade<sub>ijt</sub></em></strong>, which is the dependent variable, measured as the natural log of trade in constant 1992 dollars in a specific year (<strong><em>t</em></strong>) between a specific pair of countries (<strong><em>i</em></strong> &amp; <strong><em>j</em></strong>). The dataset covers 76 countries for the years 1961 to 1992. The data were collected by Scott Kastner for his 2007 article, “When Do Conflicting Political Relations Affect International Trade?” <em>Journal of Conflict Resolution</em> 51: 664-688.

Kastner argues that the level of trade depends on conflicting interests between countries and the strength of domestic actors who benefit from trade. Kastner cannot measure this latter variable directly, so he uses the extent of trade barriers as a proxy variable that is inversely related to the strength of pro-internationalist domestic actors.

Kastner’s theoretical argument is fundamentally interactive: he contends that while higher levels of conflict reduce trade, this effect is greatest when there are many trade barriers (indicating weak pro-internationalist interests). He estimates the following model:

where <strong><em>conflict</em></strong> measures the degree of dissimilarity between the two countries’ voting patterns in the United Nations; its range is from 0 to 1.1, with an average of 0.37

<strong><em>trade barriers</em></strong> measures policy distortions to international trade, from fixed effects estimated by Hiscox and Kastner (2002); its range is from 0.96 to 4.12 with an average of 3.42

<strong><em>interaction</em></strong> is the product of <strong><em>conflict</em>*<em>trade barriers</em></strong>; its range is from 0 to 4.27, with an average of 1.26.

For controls, you will use four variables:

<strong><em>laglnrtrade</em></strong> is the lagged dependent variable

<strong><em>lnrgdpab</em></strong> is the natural log of the product of gross domestic products of the two countries

<strong><em>lndist</em></strong> is the natural log of the distance between the two countries

<strong><em>landlocked</em></strong> counts the number of countries in a dyad (0, 1, 2) that are land-locked

<ol start="3">

 <li>Estimate the regression model and report your results.</li>

</ol>

<em>Note that Kastner clusters his standard errors by dyad, which makes his standard errors larger (and his t statistics smaller) than what you will find using ordinary standard errors. </em>

<ol start="4">

 <li>Use the results in 3. to interpret the coefficients for <strong><em>conflict</em></strong>, <strong><em>trade barriers</em></strong>. Make sure to note when the coefficients are nonsensical or at least how our ability to interpret them is impaired by the ranges of these two variables.</li>

</ol>

Next, use the results to calculate the following:

<ol>

 <li>a) the linear equation that expresses the marginal effects of <strong><em>conflict</em></strong> on trade (at all levels of <strong><em>trade barriers</em></strong>). State it first as a literal equation, and then substitute numeric values based on the regression model.</li>

</ol>

=

=

<ol>

 <li>b) the linear equation that expresses the marginal effects of <strong><em>trade barriers</em></strong> on trade (at all levels of <strong><em>conflict</em></strong>). Again, state it first as a literal equation, and then substitute numeric values based on the regression model.</li>

</ol>

=

=

<ol start="5">

 <li>Generate and display the variance-covariance matrix of the estimators. Then, use this matrix to calculate the following:</li>

 <li>a) the quadratic equation that expresses the standard error of the marginal effects of <strong><em>conflict</em></strong> on trade (across all levels of <strong><em>trade barriers</em></strong>)</li>

</ol>

s.e. () =

=

<ol>

 <li>b) the quadratic equation that expresses the standard error of the marginal effects of <strong><em>trade barriers</em></strong> on trade (across all levels of <strong><em>conflict</em></strong>)</li>

</ol>

s.e. () =

=

Kastner’s focus is on how the strength or weakness of internationalist interests moderates the effect of conflict (and not the other way around), but Berry, Golder, and Milton (2012) show that Kastner’s theory is not well supported by the data, so instead…

<ol start="6">

 <li>Treat <strong><em>trade barriers</em></strong> as the variable whose effect you are interested in, and treat <strong><em>conflict</em></strong> as the moderator. The obvious hypothesis is that <strong><em>trade barriers</em></strong> will have a negative effect on trade, and the size of this effect should be exacerbated by <strong><em>conflict</em></strong>. Show this by plotting the marginal effect of <strong><em>trade barriers</em></strong> on <strong><em>trade</em></strong> across all levels of <strong><em>conflict</em></strong>. Include the 95% confidence interval for the marginal effect.</li>

</ol>

Use the results of either (a) this plot, or (b) <em>t </em>statistics calculated for specific values of <strong><em>conflict</em></strong>, to identify regions where <strong><em>trade barriers</em></strong> has a statistically significant effect on the amount of trade in a dyad.