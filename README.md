# Exploration-of-the-UK-Gender-Pay-Gap
Classification analysis of the UK GPG

Paying women less than men is unfair and has far-reaching implications for society by contributing to the gender pay gap (GPG), women’s lower pension contributions and their higher incidence of relative poverty in later life (Whaley, 2018). The UK’s national Gender Pay Gap (GPG; 17.9%*; Equal Pay Portal, 2018) is currently higher than both the OECD and EU average (OECD=13.5%, EU=16.2%; OECD Social Policy Division, 2018). 

GPG is the difference in average hourly wage of all men and women across a workforce and refers to the uneven distribution of men and women in high/low income positions/hourly wage across a company (GOV.UK, 2018a). Whereas, unequal pay (which has been illegal since 1970; Equal Pay Act, 1970) is paying men and women differently for performing the same (or similar) work. 

In 2017, the UK launched regulation legally requiring all employers with more than 250 employees to report and publish their GPG data yearly (GOV.UK, 2018b). Making this data public is an important step towards understanding and closing the GPG.

Especially, financial services companies have been subject to public scrutiny after reporting their GPG (Gordon et al., 2018). E.g. Goldman Sachs International reported a 36.4% median GPG in 2017 (GOV.UK, 2017). Having this data public adds accountability to companies and puts pressure on them to close the GPG. 

By requiring companies to report GPG data yearly, they are encouraged to monitor and evaluate their action plans and set specific time-bound targets. An example of a company taking action to decrease their GPG after publishing their numbers is EasyJet. In the first reporting in 2017 their hourly median GPG was 45.5%. However, they addressed this imbalance by launching an initiative (i.e. the Amy Johnson Initiative; EasyJet, 2018) targeting that 20% of new cadet pilots should be female by 2020. In 2018, 13% of their pilots were women. Although, their 2018 median GPG was 47.9%, this is due to a large intake of women in the lower quartile pay bracket, who will over time rise to higher paying positions. This highlights the importance of interpreting results with caution and within context. 

The GPG data can be used to identify trends and issues within companies and sectors. Looking at statistics at sector level can help target efforts effectively. Behaviour change interventions aimed at decreasing the GPG rely on an understanding of the target group to be the most effective (i.e. no one size fits all model) (Ajzen, 2002). Target groups vary in the behaviour/culture at the root of the ‘problem’ (e.g. GPG). Therefore, it makes sense to identify groups with similar characteristics and aim interventions at this level. It is reasonable to argue that sectors/divisions largely share a culture/behaviour associated with the line of behaviour. Therefore, the Standard Industrial Classification (SIC) system used in the UK to divide companies by sectors is especially helpful in identifying which sectors need intervention and understand how to orchestrate it. 

The SIC code system is used to classify industries by a five-digit code and is used by government agencies (e.g. Companies House, ONS) to systematically identify and categorise the principal business activities of companies within the UK (ONS, 2007). The SIC codes can be grouped into progressively broader industry classifications: industry group, major group, and division (i.e. the first 2 digits indicate the major group). 

This paper will look at the reported GPG data from 2017 and 2018 and explore whether the reported GPG data can classify which sector a company belongs to. The following multilabel classification models are tested to assess which perform the best for this task: Random Forest, Knn, Naïve Bayes and Decision tree. Based on this assessment, this paper will conclude that it is not possible to reliably classify which sector a company belongs to based on its reported GPG data.

• April 2018 – Median hourly difference among all employees (both full-time and part-time)


Data:

The data used in this paper is the official UK GPG reports from the years spanning 2017-18 and 2018-19 which are publicly available online as CSV files (GOV.UK, 2019). Transparency is key, and this dataset is collected in the same way across all companies which allows for comparability. 

The data includes the following variables: mean hourly GPG, median hourly GPG, mean bonus GPG, median bonus GPG, proportion of men in the organisation receiving a bonus payment, proportion of women in the organisation receiving a bonus payment, and the proportion of men and women in each quartile pay band. 
Mean hourly GPG calculations are made by 1) adding together the hourly pay rates of all male full-time employees, 2) dividing this figure by the number of male full-time employees - this gives you the hourly pay rate for men, 3) do the same for all female full-time employees to get the hourly pay rate for women, 4) subtract the mean hourly pay rate for women from the mean hourly pay rate for men, 5) divide the result by the mean hourly pay rate for men, 6) multiply the result by 100 - this gives you the mean gender pay gap in hourly pay as percentage of men's pay (Government Equalities Office, 2017). Similar steps are taken to calculate all other measures (i.e. all numbers reflect a percentage of men's pay - if the GPG is 22% it means that women on average earn 22% less than men).

Remuneration provided otherwise than in money (e.g. vouchers) are excluded from the ordinary pay measures but are included in 'bonus pay'. Yet salary sacrifice vouchers (e.g. childcare) is not included in bonus pay but is calculated into the ordinary pay.
