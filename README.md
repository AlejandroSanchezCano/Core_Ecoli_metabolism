# Core_Ecoli_metabolism
Use ODE to study a simplified version of the core metabolism of E.coli


Metabolic networks are highly complex, so we require methods to mathematically simplify the system to understand its dynamics. Himeoka and Mitarai (doi: 10.1101/2021.07.21.453212) have explored an automated method to reduce a full set of ODEs to a core model that explains different stages of E. coli growth. This reduced model is written as


d[pep]dt=ϕ([glc]-[pep]+[pyr]+r[oaa])-(1+d)[pep]


d[pyr]dt=ϕ([pep]-[pyr]r[oaa])-d[pyr]


d[oaa]dt=[pep]-ϕ[oaa]


where [glc] = input glucose, [pep] = phosphoenolpyruvate, [pyr] = pyruvate, and [oaa] = oxaloacetate. The parameter d reflects degradation of compounds, r is related to growth/dilution effects on the concentrations of [pep] and [pyr] in the simplified model. Finally, \phi=\max\funcapply{1-\left[pyr\right],\phi_0} reflects the concentration of ATP and ADP in the cell.


The distinction between growth and dormant domains of E. coli growth are described by the concentration of ATP/ADP such that \phi=0.1 during growth and \phi\approx{10}^{-8} during dormancy. We can also take r = 0.1 and d = 10-8. Initially assume that [glc] = 1 and, to simplify matters for analysis, you could consider that [oaa] exists at steady state.


With this information to hand, use the tools taught during the course to simulate this model, observe the different dynamics between growing and dormant E. coli, assess the effect of perturbing parameters on the system dynamics, and look at how the system responds to different [glc] inputs (both constant and time-dependent).


Importantly, discuss the validity of assumptions made in the model and whether/how the model could be extended to better reflect reality. You may also wish to consider performing simulations to generate experimental hypotheses to determine how E. coli would respond to certain experimental conditions. Are you able to find any published data that supports these predicted results?
