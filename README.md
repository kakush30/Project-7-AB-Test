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

4) Click through probablity is formed from 2 variables, number of unique cookoie to click `Start free Trial` & number of unique cookies to view the overview page. Both of this collected before starting of experiment, so this is invariant. 

5) Number of users that checkout may be different because of experiment, and can be different, so this cant be choosen as invariant. But this can be Evaluation Metrics, as the difference of before & after can be meaningful for bussiness. As the Gross Conversion rate remain low that means low users checking out & enrolling. 

6) Number of users that choose the Paid service after Free Trial. It can be chooses as Evaluation Mertics in hope more people retain the course after Free service.

7) Because number of users remain enrolled past the trial, this cant be Invariant Metrics. But it can be Evaluation Metrics in expectation that after experiment it increase after experiment.

## Measuring Standardd Deviation 

![3rd img](https://raw.githubusercontent.com/kakush30/Project-7-AB-Test/master/img/Untitled3.png)

The Unit of Diversion is choosen dring design phase in order to provide the monitoring of the user experience during throughout experiment. In this experiment we able to include non-logged traffic to compute some specefic metrics of interests. In this, cookies are choosen as one diversion, for Gross & Net Conversion, the denominators are cookies. Because both use cookies as the unit of analysis, the analytical estimate would be comparable to the emperical viability. 

For retention, as unit of analysis are user-ids, non-logged in data cannot be tracked. It worth be doing an emperical estimate if time permits. 

## Sizing

With Retention, the estimate page views 4741212.

![4th img](https://raw.githubusercontent.com/kakush30/Project-7-AB-Test/master/img/Untitled4.png)
