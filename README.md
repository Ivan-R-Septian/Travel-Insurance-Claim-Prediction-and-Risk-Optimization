# **Travel Insurance Analysis: Predicting Insurance Claims for Strategic Planning**
**Ivan Robi Septian**

____________________________________________________________________________________________________________________________
## Introduction to Travel Insurance

Travel insurance is a type of insurance that provides protection during both domestic and international trips. Several companies offer travel insurance services, including AXA, Prudential, Chubb, Generali, and Sompo, among others. Many travelers consider travel insurance an essential companion due to its benefits, which protect policyholders from various risks that may occur during their journey. These benefits include:
- Medical protection and evacuation
- Compensation for baggage damage or loss
- Trip cancellation protection
- Coverage for accidents, permanent disability, death 
- And many more

#### General Terms
- Policyholder: The individual who owns the insurance policy.
- Insured: The individual or entity covered by the insurance policy.
- Premium: The amount paid by the policyholder to the insurance company for coverage.
- Claim: A request made by the insured to the insurance company for payment of benefits under the policy.
- Coverage: The amount of protection provided by the insurance policy.
- Exclusion: Specific conditions or circumstances that are not covered by the insurance policy.
- Deductible: The amount the policyholder must pay out of pocket before the insurance company pays a claim.
- Limit of Liability: The maximum amount the insurance company will pay for a covered loss.

## **Data Understanding**

The above problem will be analyzed using the **Travel Insurance** dataset. This dataset was uploaded by Zahier Nasrudin on Kaggle in 2019 and contains historical data of travel insurance users who filed claims and those who did not, based on travel insurance agencies in Singapore. The dataset can be accessed [here.](https://www.kaggle.com/datasets/mhdzahier/travel-insurance?resource=download)


### Attributes Informartion

| Attribute | Data Type, Length | Description |
| --- | --- | --- |
| Agency | object | Name of agency |
| Agency Type | object | Type of travel insurance agencies |
| Distribution Channel | object | Channel of travel insurance agencies |
| Product Name | object | Name of the travel insurance products |
| Gender | object | Gender of insured |
| Duration | Int | Duration of travel |
| Destination | object | Destination of travel |
| Net Sales | Float | Amount of sales of travel insurance policies |
| Commission (in value) | Float | Commission received for travel insurance agency |
| Age | Int | Age of insured |
| Claim | Text | No – Claim status is rejected, Yes – Claim status is accepted |


## **Bussiness Problem**
Travel insurance companies generate revenue primarily through premiums paid by policyholders. These premiums are calculated based on factors such as trip duration, destination, age of the traveler, and coverage options. By pooling the premiums from many policyholders, insurance companies can cover the claims made by a few, while investing the premium funds to generate additional income. This business model allows them to manage risks effectively and remain profitable.

Travel insurance companies rely heavily on premiums paid by policyholders for revenue. These premiums are determined by factors such as trip duration, destination, traveler age, and coverage options. The challenge is to leverage machine learning to predict which policyholders are likely to file claims in the future. By doing so, insurance companies can proactively manage risks and allocate resources effectively. Furthermore, using explainable AI, the goal is to identify the key characteristics and factors influencing claim likelihood. This understanding will enable insurers to optimize pricing strategies, improve risk assessment, and enhance customer satisfaction by offering tailored insurance products.

### **Goal**

1. **Predictive Capability**: Develop a robust machine learning model that accurately predicts the likelihood of travel insurance policyholders filing claims in the future. This predictive capability will empower insurance companies to proactively manage risks, allocate resources efficiently, and improve financial planning.

2. **Explainability and Insights**: Utilize explainable AI techniques to interpret and understand the factors influencing claim likelihood. By gaining insights into these key characteristics, insurance companies can refine their underwriting processes, optimize pricing strategies, and offer personalized insurance products that better meet the needs of their customers.

By achieving these goals, travel insurance companies can enhance their operational efficiency, mitigate financial risks associated with claims, and ultimately improve customer satisfaction through tailored insurance solutions.

### **Real Case Problem**

We are analyzing a case study from FWD Singapore, a practical example of a travel insurance provider (source: [FWD](https://www.fwd.com.sg/travel-insurance/)), which offers the following financial details:
- **Premium**: S$283.55
- **Premium**: S$327,02
- **Coverage**: S$15,000
- **Promotion**: S$30 discount

By integrating these financial parameters into our dataset, we aim to evaluate the business impact of machine learning applications in the travel insurance industry. This study seeks to understand how these parameters influence predictive modeling and strategic decision-making, enhancing business outcomes and customer satisfaction.

![FWD](https://miro.medium.com/v2/resize:fit:640/format:webp/1*cjmkK7Xb6HDPSCsvOuQAig.jpeg)

COST ANALYSIS

## Financial Analysis: Impact of Machine Learning on Insurance Claims

### Premium and Coverage Details
- **Premium**: S$283.55
- **Coverage**: S$15,000
- **Campaign Cost**: S$15 per insured

### Without Machine Learning

#### Total Premium Income
- Formula: `Premium x All Insured`
- Calculation: `283.55 x 7804 = S$2,212,824.2`

#### Total Claim Cost
- Formula: `Claim Insured x Coverage`
- Calculation: `133 x 15000 = S$1,995,000`

#### Total Promo Cost
- Formula: `All Insured x Campaign`
- Calculation: `7804 x 15 = S$117,060`

#### Total Profit
- Formula: `Total Premium Income - Total Claim Cost - Total Promo Cost`
- Calculation: `2,212,824.2 - 1,995,000 - 117,060 = S$100,764.2`

### With Machine Learning

#### Total Premium Income
- Formula: `Premium x (True Negatives + False Negatives)`
- Calculation: `283.55 x (2162 + 7) = S$615,019.95`

#### Total Claim Cost
- Formula: `Claim Insured x Coverage`
- Calculation: `7 x 15000 = S$105,000`

#### Total Promo Cost
- Formula: `All Insured x Campaign`
- Calculation: `7804 x 15 = S$117,060`

#### Total Profit
- Formula: `Total Premium Income - Total Claim Cost - Total Promo Cost`
- Calculation: `615,019.95 - 105,000 - 117,060 = S$392,959.95`

### Summary
By using machine learning, the profit increases from S$100,764.2 to S$392,959.95. This demonstrates a significant improvement in profitability, mainly due to the model's ability to minimize false negatives and thus undetected claims.

