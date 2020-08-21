# How to use the Random Module in Python

The **random module** provides access to functions that support many operations. Perhaps the most important thing is that it allows us to generate random numbers.

**Random functions**

The Random module contains some very useful functions.

```
import random
print random.randint(0, 5)
```

To get the larger number randomly just multiply it.

```
import random
random.random() * 100
```
**Choice**

Generate a random value from the sequence sequence.

The choice function can often be used for choosing a random element from a list.

```
import random
myList = [2, 109, False, 10, "Lorem", 482, "Ipsum"]
random.choice(myList)
```

**Shuffle**

The shuffle function, shuffles the elements in list in place, so they are in a random order.

```
from random import shuffle
x = [[i] for i in range(10)]
shuffle(x)
```

**Randrange**

Generate a randomly selected element from range(start, stop, step)

```
import random
for i in range(3):
    print random.randrange(0, 101, 5)
```
_______________________________________________

# What is Risk Analysis in Software Testing and how to perform it? 

The probability of any unwanted incident is defined as Risk. In Software Testing, risk analysis is the process of identifying the risks in applications or software that you built and prioritizing them to test. After that, the process of assigning the level of risk is done. The categorization of the risks takes place, hence, the impact of the risk is calculated.

**Why use Risk Analysis?**

In any software, using risk analysis at the beginning of a project highlights the potential problem areas. After knowing about the risk areas, it helps the developers and managers to mitigate the risks. When a test plan has been created, risks involved in testing the product are to be taken into consideration along with the possibility of the damage they may cause to your software along with solutions.

**The possible risks that might occurs:**

- Use of new hardware
- Use of new technology
- Use of new automation tool
- The sequence of code
- Availability of test resources for the application

**The certain risks that are unavoidable:**

- The time that you allocated for testing
- A defect leakage due to the complexity or size of the application
- Urgency from the clients to deliver the project
- Incomplete requirements

We have to take care when we are dealing with each cases such as:

- Conduct Risk Assessment review meeting
- Use maximum resources to work on high-risk areas
- Create a Risk Assessment database for future use
- Identify and notice the risk magnitude indicators: high, medium, low.

**What are these risk magnitude indicators?**

- **High:** means the effect of the risk would be very high and non-tolerable. The company might face loss.
- **Medium:** it is tolerable but not desirable. The company may suffer financially but there is a limited risk.
- **Low:** it is tolerable. There lies little or no external exposure or no financial loss.

**Risk Identification**

There are different sets of risks included in the risk identification process, and they are:

-  **Business Risks:** This risk is the most common risk associated with our topic. It is the risk that may come from your company or your customer, not from your project.
- **Testing Risks:** You should be well acquainted with the platform you are working on, along with the software testing tools being used.
- **Premature Release Risk:** a fair amount of knowledge to analyze the risk associated with releasing unsatisfactory or untested software is required.
- **Software Risks:** You should be well versed with the risks associated with the software development process.
After identifying the risks associated with your software, the next step is to assess the risks; i.e, Risk Assessment.

**Risk Assessment**

In the risk analysis process, these steps prove to be the most important one. It is said that this step is way too complex and should be tackled with the utmost care. After risk identification, assessment has to be dealt programmatically. 

**The perspective of Risk Assessment**

There are three perspectives of Risk Assessment:
- **Effect:** To assess risk by Effect. In case you identify a condition, event or action and try to determine its impact.
- **Cause:** To assess risk by Cause is opposite of by Effect. Initialize scanning the problem and reach to the point that could be the most probable reason behind that.
- **Likelihood:** To assess risk by Likelihood is to say that there is a probability that a requirement won’t be satisfied.

**How to perform Risk Analysis?**

There are three stepsto perform Risk Analysis, and they are:
- Searching the risk
- Analyzing the impact of each individual risk
- Measures for the risk identified
