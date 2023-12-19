# Kidney Transplant Analysis
matplotlib, Python, Pandas, Scipy.Stats, Numpy, Pathlib, hvplots, requests

**Challenge Synopsis:**

Our team of four students came up with a project to analyse and compare kidney transplantation between Oklahoma data and Nationwide data. This data was pulled on December 8th of 2023 at OPTN(cited below). Factors that could change kidney transplant wait times include blood types, ages, ethnicity, and gender. We determined as a group that payment time was a non-issue due to the fact that a patient must be able to pay for the transplant, blood transfusion, and follow-up treatment to be added to the wait list.

In our study we compared wait times between people living in Oklahoma and Nationwide. We used bar graphs, boxplots, and chi tests to execute comparisons.

**Questions Asked**
  - How many people in Oklahoma and in the US need a kidney transplant?
  - How long are they on the waiting list?
  - What factors affect wait times?
  - Do certain ethnicities or sexes have higher needs for kidney transplants?
  - What is the most common wait time?
  - Does blood type affect kidney transplant wait time?

**Challenges We Faced:**
- Data gathering
  
  - HIPPA greatly reduced our ability to gather more indepth information on patients and PII(Personal Identifiable Information)
  - Given the short timeframe for completion, [National Institute of Diabetes and Digestive and Kidney Diseases](https://www.niddk.nih.gov/) could not fulfill our request for datasets pertaining to our project.
  - The dataset kept including commas and quotations that didn't appear in the original dataset. Instead we coded a comma/quotation removal.
  - In our dataset, one person was listed multiple times based on how many ethnicities they identified with. These individuals had to be grouped together at not be counted more than once.

- Statistical Analysis
  - The dataset we were able to obtain used a wait time range instead of numerical values for each patient. The ranges proved to be challenging in calculating statistical analysis in any capacity. These were later transposed into numerical values or medians per category.
  - Chi-square testing did not compute in our Jupyter Notebook for ethnicities. 597/7 had too many digits for the calculation to register correctly. However we were able to find an online calculator at [GraphPad](https://www.graphpad.com/quickcalcs/chisquared2/)
  - We were unable to use t-testing because we felt that averaging out wait time ranges for kidney transplants was misleading and unethical; the larger the wait time the more drastic the difference would be between one patient to the next in that given category.
  - Data for blood type AB is very limited due to only 4% of the population being born with this type. When plotting this blood type there isn't enough data to go into depth with this information. For boxplots we could have used a logarithmic scale to potentially show more on this if we wanted to scale it down to that level. However, we didn't think this information would add to our project.

**Analysis and Conclusions**

As of December 8 2023 there were 88,767 people waiting for a kidney transplant in the USA. Of those 88,767, 597 of them reside in Oklahoma. We have rejected our null hypothesis finding that several factors contribute to longer wait times for receiving a kidney transplant. The demographics with the longest wait times had O blood type, were men, between the ages of 50-64, and were white/non-Hispanic. The median wait time is between 1 and 2 years for a kidney transplant no matter the variables.

**Our Null Hypothothesis  (H0):** Wait times are about the same for everyone who needs a kidney transplant both in Oklahoma and Nationwide.

We executed chi-square tests for each variable - age, gender, ethnicity, and blood type. By assessing the p-values, we found that they are all extremely small (basically zero) for each category essentially causing us to reject our null hypothesis.

**Our Alternative Hypothesis (H1):** Wait times are different based on different demographics such as blood type, gender, age, and ethnicity both in Oklahoma and Nationwide.

Demographics with the longest wait times were as follows:
  - Blood Type: O blood type in both Oklahoma and the USA had the longest wait times
  - Gender: Men waited longer in both Oklahoma and USA statistics
  - Age: 50-64 year olds waited the longest in Oklahoma and USA
  - Ethnicity: White/Non-Hispanic waited the longest in Oklahoma, Black waited the longest in the USA

Further conclusions we can draw from our study is that we need more information, more datasets, etc because there are far more variables that we are not able to analyze. The data we were studying only included patients who could pay for treatment but we did not explore the varying payment types. There are a whole subset of people who cannot afford treatment who need kidney transplants. These patients were not respresented in our datasets.


**CALL TO ACTION**

Thousands of people across the USA and hundreds right here in Oklahoma need a kidney transplant. YOU CAN HELP! Consider becoming an organ donor by indicating your wishes on your driver's license. Or if you would like to sign up online, start at [LifeShareRegistry](https://www.lifeshareregistry.org/register/) and follow the instructions listed there. Be sure to share your decisions with your family!

**SHARE YOUR SPARE**

You may even choose to go a step further and become a living donor. You only need one kidney to live a healthy life! Consider "sharing your spare."



**Citations:**

- Contributors:

  - [Amanda Hinkle](https://www.linkedin.com/in/amanda-hinkle-9105941b6/)

  - [Barb Rupps](https://www.linkedin.com/in/barbrupps/)

  - [Amanda Pigman](https://www.linkedin.com/in/amanda-pigman-904558227/)

  - [Cory (Chapman) Houston](https://www.linkedin.com/in/cory-houston-679447147/)

    - Instructor: [Othmane Benyoucef](https://www.linkedin.com/in/othmane-benyoucef-219a8637/)

    - Assistants: [Jacob Peroutek](https://www.linkedin.com/in/jperoutek/) [Isabella Taylor](https://www.linkedin.com/in/isabellajade/)

    - Median function instead of Mean function suggested by Ask BCS Learning Assistant
  

Datasets acquired at: [Organ Procurement & Transplantation Network](https://optn.transplant.hrsa.gov/)

Chi-square test calculation for ethnicities: [GraphPad](https://www.graphpad.com/quickcalcs/chisquared2/)

Clean Value Function for removing commas and quotations in cleaned dataset [Stack Overflow](https://stackoverflow.com/questions/73951038/how-can-i-use-this-message-to-filter) [django](https://docs.djangoproject.com/en/5.0/ref/forms/validation/)

Transpose function for easier plotting [w3resource](https://www.w3resource.com/pandas/dataframe/dataframe-transpose.php)




