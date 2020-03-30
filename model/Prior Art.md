# Prior art

Many epidemiological models (and models in other fields, like atmospheric modeling) make a subset of the relaxations or assumptions that we make. This body of literature should be explored further, but a subset of relevan papers is listed below.

Jing Li, et. al. The Failure of R0. [Comput Math Methods Med.](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3157160/)
  - Survey highlighting that R0 estimation is extremely fickle, showing how different methods of estimation can result in very different results. It shows that epidemic infection can still persist if R0 < 1, and R0 is not a measure of the necessary control effort. It also cites research showing that empirical methods of collecting r0 through contact tracing prodcues misleading estimates. It suggests that policy decisions should not be based on r0, and suggests that the urgent need is a simple but accurate measure of disease spread that can be understood by nonmathemeticians.


Katrin Haessler, et. al. A dynamic Bayesian Markov model for health economic evaluations of interventions in infectious disease. [BMC Medical Research Methodology](https://bmcmedresmethodol.biomedcentral.com/articles/10.1186/s12874-018-0541-7)
  - Engages with the idea of relaxing assumptions used in ODEs due to the impact on probabistic sensitivity analysis. It suggests that these relaxations are necessary in order to do good risk assessment. It uses a Bayesian framework for parameter calibration.
  
Laurent Hébert-Dufresne, et. al. Spread of infectious disease and social awareness as parasitic contagions on clustered networks.[arXiv](https://arxiv.org/abs/2003.10604)
  - Considers the impact of cliquish networks on contagion, and models social awareness (a type of mitigation) as a 'parasitic contagion.' The results show the 'counterintuitive' effect that networks with clustering can result in higher peak incidence than random networks. The paper highlights the need for improved data collection of awareness and methods for measuring how awareness connects to preventative behaviors.
  
 Neil Ferguson, et. al. Impact of non-pharmaceutical interventions (NPIs) to reduce COVID19 mortality and healthcare demand. [Imperial College](https://www.imperial.ac.uk/media/imperial-college/medicine/sph/ide/gida-fellowships/Imperial-College-COVID19-NPI-modelling-16-03-2020.pdf)
  - Aims to quantify the impact of suppression and mitigation strategies. It utilizes an individual-based simulation model to build groups of 'workplaces,' 'schools,' and 'households,' as well as allowing random community contact. It uses survey data for calibrations of the effectiveness of mitigation policies as well as topology. It models infectiousness as a gamma distribution assigned to individuals, but assumes a fixed r0 (with a small amount of sensitivity analysis) and leaves many other variables as fixed as opposed to stochastic. Additionally, while not stated, it seems to assume that asymptomatic individuals are not infectious. It does not use uncertainty estimates, and assumes the policies are determinstic (i.e. isolation at a fixed time after symptoms), and does not model things like case imports, but claims that the policies are robust to r0 and severity and makes recommendations based on this large set of assumptions.
  
Lingcai Kong, et. al.. Modeling Heterogeneity in Direct Infectious Disease Transmission in a Compartmental Model.[Int J. of Environ Research and Public Health](https://pubmed.ncbi.nlm.nih.gov/26927140/)
  - Uses a common SEIR compartmental model to model SARS, but adds a transmission function based on the Negative Binomial Distribution. It shows that given a fixed mean contact rate and fixed infectiousness per contact, the heterogeneity of mixing (i.e. the variance/tailedness of the distribution) is a major driver in changing disease propagation. This result still gives a fixed r0, but the peak size, transmission speed, and peak dynamics are all hugely dependent on this mixing parameter. It fits this model to historical SARS data, showing that modeling mitigation simply as a change in heterogeneity fits daily cases well. It makes the concession that migitation measures likely change the impact of contact (i.e. more hygiene means the effective transmission of a given contact is lower). It does not split the population into demographic subgroups, and does not use a WAIFW style ("who acquires infection from whom") isolation matrix. 
  
Marc Barthélemy, et. al. Dynamical Patterns of Epidemic Outbreaks in Complex Heterogeneous Networks. [J. Theor Biol](https://pubmed.ncbi.nlm.nih.gov/15862595/)
  - Builds 'complex heterogenous networks,' believing that dynamics are related to the second moment degree distribution. It postulates that R0 is actually >1 in any heterogenous network, and every infection has some probability of generating a major outbreak. It finds that in both uncorrelated and correlated scale-free networks, epidemic incidence can rise virtually instantaneously. It then simulates a real world network with preferential attachment, and shows that heterogeneity makes it hard to determine the r0 and accelerate propagation. In these heterogenous networks, infection first takes control of large degree vertices and then cascades to lower degree vertices. It suggests that control strategies should focus on population hubs, and suggests that global surveillance of network structure is critical to epidemic control.

T J Hagenaars, et. al. Spatial Heterogeneity and the Persistence of Infectious Diseases. [J. Theor Biol](https://pubmed.ncbi.nlm.nih.gov/15234202/)
  - Simulates spatially heterogenous populations, and starts to explore the interplay of 'patch-level' dynamics as an alternative to a full model. This formulation is similar to finite element methods and finite difference methods in other fields. 

A finite-difference method for the variable coefficient Poisson equation on hierarchical Cartesian meshes, Alice Raeli, et. al. [J. Computational Physics](https://www.sciencedirect.com/science/article/pii/S0021999117308343)
  - Shows that it is possible to use hierarchical meshes when geometry is changing to model complex dynamics with less computation in finite differences models. While not directly relevant to epidemiological modeling, it suggest that hierarchical compositions of compartmental models for different populations could be useful for simulation. 