# CompetingRates
A competing rates model for seroprevalence in the Democratic Republic of Congo that combines analysis of vaccination surveys, case reports, ans serosurveys to estimate the force of infection, vaccination hazard, and vaccine efficacy. The seroprevalence of an individual is a result of the _sum_ of the vaccination hazard and force of infection, both integrated to that individual's age.

### Code:
* Generating posterior samples (MCMC code): Stable_DRC.ipynb and BF_DRC.ipynb. The first uses Weibull functions to model both the force of infection and vaccination hazard. The second is for calculating the Bayes factor between a constant force of infection, and a force of infection that is a Weibull plus a constant. Both use the PTMCMC sampler from Justin Ellis.
* BF_postproc.ipynb: takes samples generated from BF_DRC and calculates the actual Bayes factor between the two models using the Savage-Dickey density ratio.
* Figures.ipynb: what it says on the tin. The figures used in the paper are all generated in this notebook.
* FakeData.ipynb: takes data from our simulations and adjusts them to have the desired vaccine efficacy, and then generates observables akin to those in the real-world data.

### Data
* DRC_urban_* contains raw output from our disease simulations. These csv's need to be read in to FakeData.ipynb in order to generate data for analysis.
* FakeData50* are the actual simulated datasets used in analysis. veff* indicates the fractional vaccine efficacy used to generate each csv.
* foi_injected is the force of infection from the simulation
* pvaccCov* is the probability of vaccination for two different vaccine efficacies.


