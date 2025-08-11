# GLASST-Outputs

# Table of Contents

1.  [ITHIM V1](#ITHIM-V1)
2.  [ITHIM V2](#ITHIM-V2)

## 1. Integrated Transport and Health Impact Model (ITHIM)

The majority of Health Impact Assessment (HIA) models are characterized by their simplicity, frequently employing counter-factual exposures as opposed to simulations. The sequence of changes starts with modifications in transport activities (the source), exposures, and finally health impacts. Such studies frequently fail to elucidate the mechanisms through which such reductions could be achieved. ITHIM provides a different approach. It simulates individual behaviours, capturing heterogeneity in the population, and their changes in non-spatial manner and then calculates the impacts of such changes on health. It provides clear and well defined mechanisms on how the change - which could be driven by policies, affects population and its subgroups.

### **ITHIM Global Version 1** {#ITHIM-V1}

(daylong travel data). This model builds on older ITHIM versions that take inputs as a single day travel behaviour. We advanced this model in the following ways:

1.  Thorough checking of all inputs - especially focusing on the travel behaviours by:

    1.  Number of trips per person
    2.  Coverage - the geographical extant
    3.  Demographics - based on age and gender
    4.  Distribution to identify expected time spent/distances

2.  For physical activity, we have brought innovations in three ways:

    1.  To built a better representation and robustness of individualized physical activity profiles, we have developed mechanisms to supplant non-travel related physical activity using processed physical activity survey.
    2.  We used the latest evidence that shows a non-linear relationship for health outcomes/disease and their impacts on physical activity using dose-response relationship (link to paper)
    3.  To cater the effect of non-linearity, and using WHO's recommended level of physical activity, we delved into further details and showed impact of these levels on health impacts (link to results checking)

3.  For PM 2.5 Air Pollution, we developed a protocol that:

    -   Uses the latest evidence that is generalisable, we built a detailed profile of individuals based on their travel and non-travel activities throughout the day, while also taking account of ventilation rates and then quantified the impact of such in what-if scenarios.

4.  Combined effect of physical activity and air pollution

    -   Using exposures, we calculated the joint effect of physical activity where more Active Travel usually means better health outcomes, and PM 2.5 air pollution, which works in opposite manner, as more Active Travel usually means more exposure to harmful environment.

### **ITHIM Global Version 2** {#ITHIM-V2}

(using a week-long travel data) ITHIM Global Version 1 was built around single-day travel surveys, but these came with significant limitations. In many regions, such data simply is not available, and where it is, the quality is often poor—for example, surveys frequently fail to capture walking trips to public transport. Moreover, relying on a single day of travel data does not accurately reflect typical weekly travel patterns. Beyond these issues, Version 1 also required a large number of input parameters and data sources, which made it complex to use and limited its practicality outside of academic research.

To address these challenges, we developed ITHIM Global Version 2. This updated version reduces the number of required parameters, thereby lowering data dependency and improving robustness in settings with limited or lower-quality data. It also streamlines the use of external data sources, including a simplified approach to modelling background physical activity. Crucially, Version 2 incorporates week-long travel data generated through machine learning predictions, offering a more realistic picture of travel behaviour. The result is a smaller, faster model that is easier to set up and run, making it far more accessible and adaptable for a wider range of applications.

1.  Using machine learning to generate a week-long travel data. We developed a generative approach to create synthetic travel surveys for multiple cities worldwide, addressing critical gaps in traditional travel survey methodologies. The approach tackles issues such as one-day surveys (as opposed to seven days), underreported short trips, the absence of detailed stages for public transport (e.g., access and egress modes), insufficient survey sample sizes, and the lack of surveys or restricted access to data in many cities. Our method, based on econometric models and machine learning, aims to overcome these limitations by generating comprehensive, representative travel data. The workflow consists of three key steps:
2.  Person-based weekly trip generation: We generate weekly travel patterns for individuals, capturing a broader temporal scope than traditional one-day surveys to better reflect travel behaviour.
3.  Incorporation of trip distances and times: Trip travel distances and times are assigned, accounting for the influence of urban environments, ensuring realistic spatial characteristics.
4.  Trip mode assignment: Travel modes are determined based on trip features (e.g., travel time) and the characteristics of the trip maker, enabling accurate representation of mode choice dynamics.

A training dataset covering 28 cities was utilised to develop the models, with Bogotá selected as a use case for testing. The results demonstrate that key statistics, such as weekly trip rates, average travel times, mode shares by age and gender, and trip length distributions by modes, have been systematically compared with observed data. These comparisons show good matching accuracy, highlighting the potential of the approach to capture underlying trip patterns effectively. The method can potentially be tested in other study areas to further validate its robustness and applicability. The scripts are publicly available at: <https://github.com/Public-Health-Modelling-Cambridge/travelBehaviour>.

1.2.2 Implementation of ITHIM Global Version 2 Link plus workshop

2.  MSLT Approach

We developed open source scripts for the multi-state life table approach (link repository) and applied in international settings (link study) and developed visualisation tools (link visual one and link visual two). In our international applications with included economic values and financial costs to address use cases needs in relation to value of statistical life and potential savings in health care costs of shift to active modes of transport. We developed open access tools to facilitate modelling of diseases transitions in cohort and microsimulation modelling of chronic diseases in the absence of publicly available data. Our tool is available as an R package (package) and related publication (disbayes). We developed a microsimulation health model and are in the final validation stages (link to repository).

4.  Uncertainty and Value of Information (VoI) analysis
