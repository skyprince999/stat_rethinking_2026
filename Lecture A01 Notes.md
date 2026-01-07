##Lecture A01 Notes

###Week: 6th Jan 2026

Source:

https://www.youtube.com/watch?v=ztbYkBPDOgU


- Scientific theory ::: science before statistics
- For statistical models to produce scientific insight, they depend ypon scientific/casual models
- Meaning of statistical analysis is not found in the data but rather in theories


### Core Bayseian Workflow

(_increasing complexity_)

<img src="homework/Core Framework_1.jpg" alt="Alt text" width="50%" height="auto">

<img src="homework/Core Framework_2.jpg" alt="Alt text" width="50%" height="auto">

<img src="homework/Core Framework_3.jpg" alt="Alt text" width="50%" height="auto">

- Prior model checking: to check if the model is correct before its modeled , scientific sense
- Posterior model checking: to check after the model has been created . After the data has been "fitted"
- Parameter estimation:
  
           - marginal effects (statistical averaging)
           - causal error estimation
           - sensitivity analysis


We start from the left where we start with Generative models (_model that generates synthetic data_) and Estimands (_which is what you want to find_) Estimands can be causal estimands. 

###Causal Inference
- Causal inference in Data Science/ML has a very narrow meaning -- _mechanistic_ 
- In statistical it is a specific form of prediction which is the cause of intervention in a system
- Imputation view of causal inference -- is that we may be able to guess what would have happened if things would have been different
- Explanatory version ::: is *why* something happened

*Causal Prediction* 
when trees blow in the wind we know that its because of the moving air. We are not understanding the mechanisms of why it moves (fluid mechanics) BUT the consequence  of moving air (wind) is causing the trees to move 
Here we know what causes something to happen. 

*Causal Imputation*
- If we understand the system and the causes -- we can impute counterfactual outcomes 
- Things that did not happen, but what if it happened then what could be the outcome
- this is closely related to intervenist view -- which is forward projection, vs imputation which is backward projection 

*Causal Explaination*
- explain past events
- _why did some event happen_ why did the glaciers retreat 

*Causal Interventionist*

  
###Statistical Model 
- Extracts information from a sample 


- Bayesian vs Frequentism :: Bayseian has prevailed
