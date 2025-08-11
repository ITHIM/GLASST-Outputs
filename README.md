# GLASST-Outputs
Brings together outputs of the GLASS project implemented from 2018 to 2025 [say more on GLASST]

A significant output of the GLASST project was to advance models for the assessment of the health impacts of urban transport

We focused on two modelling approaches: the Comparative Risk Assessment (CRA) approach and the Multi-Stage Life Table (MSLT) approach

Paragraphs introduces the problem that derive innovation in transport and health development
- Hightlight ithim v1 with limitations
  Thorough checking and harmonisation protocol and applied
  Robust physical activity (Using of non-linear Physical activity dose-reponse and impact of censoring according to WHO's guidelines)
  Robust asessment of air polllution  
  
- Hightlight ithim v3 with limitations
  - Disease interaction and change in exposures over time
  - aging

1. Comparative Risk Assessment (CRA) Approach
The CRA approach to health impact modelling systematically evaluates and compares the risks posed by different hazards or interventions...

We have made advancements in two models that use the CRA approach: ITHIM Global Version 1 (single day-long travel data) and ITHIM Global Version 2 (Week-long travel data)

1.1 ITHIM Global Version 1 (daylong travel data)
- This model builds on older ITHIM versions that take inputs as a single day travel behaviour. We advanced this model in the following ways:
 - Use of new PA DRF with different cut-off points 
 - 
	
1.2 ITHIM Global Version 2 (using a week-long travel data)
ITHIM Global Version 1 was built around single-day travel surveys, but these came with significant limitations. In many regions, such data simply is not available, and where it is, the quality is often poor—for example, surveys frequently fail to capture walking trips to public transport. Moreover, relying on a single day of travel data does not accurately reflect typical weekly travel patterns. Beyond these issues, Version 1 also required a large number of input parameters and data sources, which made it complex to use and limited its practicality outside of academic research.

To address these challenges, we developed ITHIM Global Version 2. This updated version reduces the number of required parameters, thereby lowering data dependency and improving robustness in settings with limited or lower-quality data. It also streamlines the use of external data sources, including a simplified approach to modelling background physical activity. Crucially, Version 2 incorporates week-long travel data generated through machine learning predictions, offering a more realistic picture of travel behaviour. The result is a smaller, faster model that is easier to set up and run, making it far more accessible and adaptable for a wider range of applications.

1.2.1 Using machine learning to generate a week-long travel data
We developed a generative approach to create synthetic travel surveys for multiple cities worldwide, addressing critical gaps in traditional travel survey methodologies. The approach tackles issues such as one-day surveys (as opposed to seven days), underreported short trips, the absence of detailed stages for public transport (e.g., access and egress modes), insufficient survey sample sizes, and the lack of surveys or restricted access to data in many cities. Our method, based on econometric models and machine learning, aims to overcome these limitations by generating comprehensive, representative travel data. The workflow consists of three key steps: 

Person-based weekly trip generation: We generate weekly travel patterns for individuals, capturing a broader temporal scope than traditional one-day surveys to better reflect travel behaviour. 

Incorporation of trip distances and times: Trip travel distances and times are assigned, accounting for the influence of urban environments, ensuring realistic spatial characteristics. 

Trip mode assignment: Travel modes are determined based on trip features (e.g., travel time) and the characteristics of the trip maker, enabling accurate representation of mode choice dynamics. 

A training dataset covering 28 cities was utilised to develop the models, with Bogotá selected as a use case for testing. The results demonstrate that key statistics, such as weekly trip rates, average travel times, mode shares by age and gender, and trip length distributions by modes, have been systematically compared with observed data. These comparisons show good matching accuracy, highlighting the potential of the approach to capture underlying trip patterns effectively. The method can potentially be tested in other study areas to further validate its robustness and applicability. The scripts are publicly available at: https://github.com/Public-Health-Modelling-Cambridge/travelBehaviour.  

1.2.2 Implementation of ITHIM Global Version 2
Link plus workshop

2. MSLT Approach

We developed open source scripts for the multi-state life table approach (link repository) and applied in international settings (link study) and developed visualisation tools (link visual one and link visual two). In our international applications with included economic values and financial costs to address use cases needs in relation to value of statistical life and potential savings in health care costs of shift to active modes of transport. We developed open access tools to facilitate modelling of diseases transitions in cohort and microsimulation modelling of chronic diseases in the absence of publicly available data. Our tool is available as an R package (package) and related publication (disbayes). We developed a microsimulation health model and are in the final validation stages (link to repository).  

4. Uncertainty and Value of Information (VoI) analysis
