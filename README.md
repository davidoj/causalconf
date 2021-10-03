
Motivated by the need to deal with vagueness found in causal models, this paper takes a close look at trandom variables probability spaces and Markov categories.

# Introduction (1pg)

Two widely used approaches to causal modelling are \emph{graphical causal models} and \emph{potential outcomes models}. Graphical causal models, which include Causal Bayesian Networks and Structural Causal Models, provide a set of \emph{intervention} operations that take probability distributions and a graph and return a modified probability distribution \citep{pearl_causality:_2009}. Potential outcomes models feature \emph{potential outcome variables} that represent the ``potential'' value that a quantity of interest would take under the right circumstances, a potential that may be realised if the circumstances actually arise, but will otherwise remain only a potential or \emph{counterfactual} value \citep{rubin_causal_2005}.

One challenge for both of these approaches is understanding how their causal primitives -- interventions and potential outcome variables respectively -- relate to the causal questions we are interested in. This challenge is related to the distinction, first drawn by \citep{korzybski_science_1933}, between ``the map'' and ``the territory''. Causal models, like other models, are ``maps'' that purport to represent a ``territory'' that we are interested in understanding. Causal primitives are elements of the maps, and the things to which they refer are parts of the territory. The maps contain all the things that we can talk about unambiguously, so it is challenging to speak clearly about how parts of the maps relate to parts of the territory that fall outside of the maps.

[...]

# Probability (10pg)

 - Markov categories
 - With variables

# See-do model (1pg)

 - See-do models are two-part models: observations, (decision->consequence)
 - They arise from a stylised decision problem
 - And are closely related to classical statistical decision theory

# See-do models solve a subproblem of decision problems (2pg)

 - Task: take data, output decision, maximise utility
 - Via comb decomposition theorem: we get a see-do forecast
 	- + representation theorem: see-do model
 	- open question: vague probability decision problem -> see-do model?
 - See-do model + loss -> Wald statistical decision problem
 	- Other connections to decision theory: see-do model + determinism + rectangular field -> Savage consequence model
 	- open question: causal/evidential decision theory?

# Causal modelling approaches arising under see-do models

 - Triviality: Y independent of X given D, H
 	- What relation between Y and X?
 - Triviality: Y independent of D given X, H
 	- What relation between Y and D?

## Causal graphical models (3pg)

 - Assume there exists a partial ordering s.t. we have sequence of mostly independent and identical factors  + known replacement of remaining factors
	- Then: CBN
 	- There are probably other derivations
 	- Given a particular partial order: yields inductive hypothesis

## Potential outcomes (3pg)

 - First, representation theorem: assume (determinism), extendability, functional exchangeability
 	- Then: representation with (deterministic) counterfactuals
 - This isn't what potential outcomes models are usually doing!
 - Instead: assume independent and identically distributed potential outcomes functions
 	- Given a particular independence structure: yields inductive hypothesis

# Discussion (2pg)

 - PO representation follows from modelling sequences of ``suppositions''....but no-one ever does that
 - Using a latent PO representation does not imply we are modelling a sequence of suppositions
 - What we are actually modelling is closely related to the choice of set $D$, not to latent variable representation, and $D$ is not prescribed by either modelling approach
 - Consider: ``effect of an intervention on BMI''
