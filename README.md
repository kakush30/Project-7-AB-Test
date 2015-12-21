# A-B Testing

#### Experiment

Udacity experimented a change by adding a `Start Free Trial` button. Each visitor asked with how mnuch time they devote for a course. If the student indicate fewer than 5 hours per week than a message would appear saying `Udacity courses usually require a
greater time commitment for successful completion`, and indicating student might like to access free course material. 

## Experiment Design

Invariant Metrics: Number of Cookies, Number of Clicks

Evaluation Metrics: Gross Conversion, Retention, Net Conversion

![1st img](https://raw.githubusercontent.com/kakush30/Project-7-AB-Test/master/img/Untitled1.png)

![2nd img](https://raw.githubusercontent.com/kakush30/Project-7-AB-Test/master/img/Untitled2.png)

1) Number of cookies counted before the studennt click `Strat Free Trial` and not affected with Experiment, so invariant metrics.

2) Number of users can be different before & after showing the `message`. Thus it cannot be invariant metrics. 

3) Number of clicks is invariant, because it counted before the experiment. 

4) Click through probability is formed from 2 variables, number of unique cookoie to click `Start free Trial` & number of unique cookies to view the overview page. Both of this collected before starting of experiment, so this is invariant. 

5) Number of users that checkout may be different because of experiment, and can be different, so this cant be  chosen as invariant. But this can be Evaluation Metrics, as the difference of before & after can be meaningful for business. As the Gross Conversion rate remain low that means low users checking out & enrolling. 

6) Number of users that choose the Paid service after Free Trial. It can be chooses as Evaluation Mertics in hope more people retain the course after Free service.

7) Because number of users remain enrolled past the trial, this cant be Invariant Metrics. But it can be Evaluation Metrics in expectation that after experiment it increase after experiment.

## Measuring Standard Deviation 

![3rd img](https://raw.githubusercontent.com/kakush30/Project-7-AB-Test/master/img/Untitled3.png)

The Unit of Diversion is chosen during design phase in order to provide the monitoring of the user experience during throughout experiment. In this experiment we able to include non-logged traffic to compute some specific metrics of interests. In this, cookies are chosen as one diversion, for Gross & Net Conversion, the denominators are cookies. Because both use cookies as the unit of analysis, the analytical estimate would be comparable to the empirical viability. 

For retention, as unit of analysis are user-ids, non-logged in data cannot be tracked. It worth be doing an empirical estimate if time permits. 

## Sizing

With Retention, the estimate page views is 4741212.

But the days require for this experiment with even max traffic of 1 would be 4741212/40000 = 119 days. As time is too long, its best to remove Retention from experiment. 

Now, the days required would be 685325/40000 = 17 days.

![4th img](https://raw.githubusercontent.com/kakush30/Project-7-AB-Test/master/img/Untitled4.png)

![5th img](https://raw.githubusercontent.com/kakush30/Project-7-AB-Test/master/img/Untitled5.png)

I chooses to divert the full traffic, as it reduce the number of days.

## Experiment Analysis

#### Sanity Check

![6th img](https://raw.githubusercontent.com/kakush30/Project-7-AB-Test/master/img/Untitled6.png)

The observed values are in 95% confidence interval. Sanity Passed. 

## Result Analysis

![7th img](https://raw.githubusercontent.com/kakush30/Project-7-AB-Test/master/img/Untitled7.png)
![8th img](https://raw.githubusercontent.com/kakush30/Project-7-AB-Test/master/img/Untitled8.png)

#### Summary 

I discarded the use of Bonferroni correction in this experiment as it is very conservative. As we are using multiple metrics, that means considering multiple metrics together and all of them need to be significant.  For that Bonferroni is not designed. In this project multiple metrics need to be significant, so Bonferroni not going to be helpful.

The two metrics share the variables like cookies and user-id, they are somewhat correlated to each other. If in improvement, the experiment cause to add or minus a metric, that it also going to affect the other metric too. 

The alpha individual would be 0.025 for each of them. 

alpha individual = 0.05/2 = 0.025

There was no discrepancy between the hypothesis test and sign test. 

#### Recommendations

I done two hypothesis test, one was the Gross Conversion & other Net Conversion. 

Gross Conversion: The Gross Conversion definition is it is the ratio of the number of users enrolling in the course to the number of user who clicked Start Now Button. As the pop-up page recommend the minimum time required per week to complete this course, it reduce the total number of users enrolling for free Trial. Also the coaches able to concentrate on less number of students, and able to convert them from Free Trial to Paid Service. 

Net Conversion: The Net Conversion definitionis the number of users who enrolled for the Free Trial and make their first payment to the number of users who clicked the start free trial button. There is no statistically change in it 

My recommendations on this is that the Gross Conversion actually showing positive results and frustrated students left because they dont have enough time. In Net Conversion there is no statistically significant change, but confidence intervel does include the negative of the practical significance boundary. There is possibility that the number went down to an amount that matter to bussiness.                 

## Follow-Up Experiment

This Experiment is based on student that is about to pay there first payment, that is they are in free service. 

For reducing the attrition rate in early of course, that is those students who left the course early because they are unknowledgeable about pre requisite leanings.

For that we need a course or a Project during the Free Trial, so the users able to get an idea what prerequisite knowledge they should know & and what the course is all about. 
The system also need an auto grader so Coaches spend more time to help those users who passed this project and continued in the Course or are in Paid Servie. 

The motive of this Hypothesis is that Udacity able to know the creamy layer of users and Coaches able to devote more time on those users who are actually interested in the Course. 
The unit of diversion would be user-id as they are already registered in Free Trial. 

Invariant Metrics: 

Number of users enroll for Free Trial: As the purposes and target of this experiment on those who already enrolled in free Trial, and about to pay there first payment.

Evaluation Metrics: 

Net Conversion : The net conversion maybe drop or remain low because of Precourse Project, as this passes by those who clear it, and only allow creamy layer to go further.

Course Completion Ratio: The Course Completion Ratio are those users who completed the Course divided by total users who paid there first payment. The purpose for this to predict the Precourse Project affected the Completion Ratio is positive or negative . This Metric maybe remain high, as only those student able to get in paid service who are really interested about the course.
