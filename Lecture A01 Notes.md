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

### Causal Inference
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

  
### Statistical Model 
- Extracts information from a sample 


Bayseian models are generative. But realistic analysis involves measurement error, missing data, latent variables and regularizations 
- Bayesian vs Frequentism :: Bayseian has prevailed, there are no stats wars!

The real battle is scientific modeling 

Statistical modeling requires a lot of complex workflows. But the good practice is to always start with simpler models. Comparing simpler models with the final model helps us understand how these models work. 

- start with the basics. interesting analogy of drawing an owl from starting with drawing circles
- you are first starting with a scaffolding
- building ladders that you will climb


### How to take a sample from a population 
- How should we use a sample
- How to produce a summary
- How to represent uncertainity

Process of Bayseian updates (as new samples come in, how does the density graph shift) -- distribution assumptions being that its normal 

*Example of calculating the proportion of the Earth thats covered with water* 
- Generative model: Is a globe tossing model, which randomly generates a point on the globe and checks if its land or water
- Estimand: The question which we are trying to answer: _Proportion covered with water_ 
- Assumption: is that each sample is random and not correlated in any way

### Globe Toss Function 

In R language 
```
sim_globe <- function( p=0.7, N=9) {
sample( c("W", "L"), size=N, prob=c(1, 1-p), replace=TRUE) 
}
```

Converted to Python
```
import random

def sim_globe(p=0.7, N=9):
    """
    Simulate tossing a globe N times.
    
    Parameters:
        p (float): Probability of water ('W')
        N (int): Number of tosses
    
    Returns:
        list: Sequence of 'W' and 'L'
    """
    return random.choices(
        population=["W", "L"],
        weights=[p, 1 - p],
        k=N
    )

```

Test your code with extreme inputs/_settings/edgecases_ p=1, p=0.5 etc.. 


Garden of Forking data

<img src="homework/garden of observation data.jpg" alt="Alt text" width="50%" height="auto">
  
