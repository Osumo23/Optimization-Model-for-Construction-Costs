## **Optimization Model for Construction Costs**

## **Abstract**

The study looks at a linear programming approach towards solving an optimization problem, specifically a cost minimization problem. A company is faced with a problem of determining the number of trucks it needs to lease for construction to continue. The linear programming approach is able to meet all the requirements that are specified and able to stay within the bounds that were specified by the owner of the company

## Introduction

There are various decisions that go into management of a construction company. The decisions range from the duration of time it would take to complete the project, the number of men required for the job, the working hours, the purchase, movement and storage of construction material and the number of vehicles needed. Some of the construction companies are not big enough or some projects that construction companies are given are sometimes too large therefore, they have to outsource from other companies or lease some of the requirements from leasing companies.

Reep Construction Company wins a construction bid and is estimated to complete the project by four months. In that time, the company needs a number of trucks for use, however, the company despite having twenty trucks from a leasing agreement, they are all not available. The owner is therefore required to agree to another lease agreement to get the extra number of trucks. Another decision that the manger of the construction company is managing the various costs that would be incurred from the fuel costs, the workers pay that is determined by how long the project is estimated to take for completion and the working hours. The owner is determined to keep his employees and is willing to a short-term lease agreement. This study&#39;s objectives are to find the optimal leasing plan, the costs associated with the optimal leasing plan and the cost it takes to maintain the project without having to lay off its employees.

## Data Presentation

The details for this project include the following. The company estimates that it will take four months to complete the project. The first month requires ten trucks, the second month twelve trucks, the third fourteen trucks and the last month eight trucks. The company has in place long term lease that gets them 20 trucks, however, not all trucks will be available for this particular project as they are in use for other jobs for the company. However, one truck will be available in the first month, two trucks will be available in the second month, three and one trucks will be available for the third and fourth month respectively. Hence requiring new trucks for the project.

The long-term leasing contract charges $600 per truck. The company pays $20 per hour and the fuel costs of the trucks are around $100. The company is not responsible for maintenance costs, they are handled by the leasing company. The construction company plans for its workers to work 8 hours a day for days a week, and four weeks a month. The owner of the construction company only intends to enter into a short-term leasing contract, since they include the cost of both the driver and the truck and also, he does not have to pay for the construction job. The following are costs estimated for each of the four months cover the lease of a truck and driver:

| **Length of Lease** | **Cost Per Month** |
| --- | --- |
| **1** | 4000 |
| **2** | 3700 |
| **3** | 3225 |
| **4** | 3040 |

The objective of this study is to get a lease that minimizes the cost of meeting the monthly trucking requirements. The company also does not intend to lay off its employees.

## Model Specification

Let:

Xij – Be the number of trucks leased for the short period in month i for a period of j months

Yi - Be the number of trucks obtained for the long-term lease that are used in month i.

The monthly cost of fuel is 20\*$100 = $2000.

The monthly cost for the short term leased trucks are as indicated below (The cost will include the fuel cost of $2000):

| **Trucks** | **Cost** |
| --- | --- |
|
 | $4000 + $2000 = $6000 |
|
 | 2($3700) + $2000 = $9400 |
|
 | 3($3225) + $2000 = $11675 |
|
 | 4($3040) + $2000 = $14160 |

Monthly cost for long term lease: Since the owner of Reep Construction company insists on the no lay-offs policy, the only long-term cost will be that of fuel: with is a monthly $2000.

The objective function for the cost of leasing the company becomes:

Minimize:

The following are the constraints:

The minimization linear programming model was run through the software R (R Core Team, 2021). and was solved using the package lpSolve (Michel Berkelaar and others, 2020).

## Results

**Final value (z)**

lp (&quot;min&quot;, f.obj, f.con, f.dir, f.rhs)

Success: the objective function is 151660

The cost associated with the optimal leasing plan is $151660 with the no lay off policy.

The following were the coefficients of the objective function, these could be used to obtain the costs that are associated with the optimal leasing plan:

| Coefficient | value |
| --- | --- |
| **x11** | 0 |
| **x12** | 0 |
| **x13** | 3 |
| **x14** | 6 |
| **x21** | 0 |
| **x22** | 0 |
| **x23** | 1 |
| **x31** | 1 |
| **x32** | 0 |
| **x41** | 0 |
| **y1** | 0.999999999999999 = 1 |
| **y2** | 2 |
| **y3** | 3 |
| **y4** | 1 |

The above table indicates the number of trucks that would be needed from the short-term leasing contract. The company will need to lease three trucks in the first month for three months, six trucks in the first month for four months. In the second month, the owner will need to lease one truck for three months and in the third month, he will also need to lease one truck for one month. In the fourth month he not need to lease any trucks. Note that the number of trucks from the long-term lease has remained the same, as indicated in the question which suggests that this model is accurate.

Therefore, in the first month the following will be the costs (Second part is the fueling cost for the months the trucks will have been leased:

6\*$3040 + 6\*$100\*4 = $20, 640

3\*3225 + 3\*$100\*3 = $10575

The total cost in the first month from short term lease is $31215

In the second month, he will need to lease one truck for three months.

1\*$3225 + 3\*$100 = $3325

In the third month, the company owner will lease one truck for one month, therefore the estimated costs will be:

1\*$4000 + $100 = $4100.

## Conclusion

The model was able to meet the requirements the owner of the construction company specified. That is found the optimal cost when from the short term and long-term leases. The model gave the added advantage that they specified the number of trucks that were required from the short-term leases. The owner of the company can therefore calculate the costs for each month including the fueling cost for the period the trucks will be leased. The model was able to remain bounded by the no layoff policy.

The model can be adjusted to meet the user&#39; s requirements and it is non-parametric, which means there is no defined number of parameters that a user needs to meet to apply the model, therefore versatile in the situations where custom calculations as was in this study.

REFERENCES

R Core Team (2021). R: A language and environment for statistical computing. R Foundation for Statistical Computing, Vienna, Austria. URL [https://www.R-project.org/](https://www.R-project.org/).

Michel Berkelaar and others (2020). lpSolve: Interface to &#39;Lp\_solve&#39; v. 5.5 to Solve Linear/Integer Programs. R package version 5.6.15.

https://CRAN.R-project.org/package=lpSolve