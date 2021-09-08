

Researchers in the field of causal inference will often choose a causal framework as one of the first steps of their investigations, or in some cases, one of the first steps of their careers. One could postulate that ``causal inference'' is what one does when one does work using a causal modelling framework. We argue that ``causal inference'' is better understood by the kind of \emph{questions} people work on rather than the kind of framework people use to answer them. \citet{pearl_book_2018} has proposed a three-level hierarchy for classifying causal questions: at the bottom are ``seeing'' questions followed by ``doing'' questions with ``imagining'' questions at the top. We propose an alternative characterisation: ``ordinary statistical questions'' are questions involving data that are answered by distributions on a given set \todo{or something like that; it could also be functions of a distribution like a maximum likelihood estimate or a p-value} while ``causal statistical questions'' are questions involving data that are answered by stochastic functions with given domain and codomain. Potential outcomes and graphical models are features of modelling frameworks, while interventions and counterfactuals are features of causal problems. We show how both potential outcomes and causal graphical models arise in \emph{see-do models}, a generic modelling framework we introduce that addresses causal questions in general, as we define them. We hypothesise that some confusion about interventions and counterfactuals arises from attempts to understand them as features dictated by the modelling framework rather than by the problem under investigation.


# Introduction (1pg)

 - When people write about causal inference, they overwhelmingly say that what they're trying to figure out is e.g. the treatment effect or the interventional distribution. Few to no examples of ``here is our problem, here is how we're going to model it'
 - The ``decision theoretic approach to causality'' (Dawid, Heckerman, Rohde & Lattimore) is an example of a ``problem first'' approach: ``our problem is to make a good decision. How do we do it?''
 - A \emph{decision} theoretic approach seems to rule out counterfactuals, because we can't decide to have done something different instead, but the problem first approach does not rule out counterfactuals: ``our problem is to answer some question about what would have happened. How do we do it?''
 - On terminology: we choose terms like ``hypothesis'', ``observations'' and ``see-do model'' because we think it is easier to understand the maths with a vague notion of what it could be used to model. However, we think the maths is more important than the words we use to describe it! See-do models can still model things better described by ``state'' instead of ``hypothesis'' or by ``supposition'' instead of ``decision''.

# Probability (1pg)

 - Discrete probability
 - Probability <-> positive normed vector, Markov kernel <-> positive matrix with row sum 1
 - Pictures
 - Variables w/Markov kernels instead of probabilities
 	- Labels <-> random variables
 	- Ambiguity regarding ambient space

# See-do model (1pg)

 - See-do models are two-part models: observations, (decision->consequence)
 - Postulate: causal inference problems are problems that can be modeled with see-do models
 	- ``causal'' problems and ``inference'' problems, broadly construed, could be a much larger set!

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
