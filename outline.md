# When does one variable have a probabilistic causal effect on another?

When can one variable have a probabilistic causal effect on another?
  - Motivating example: when can "body mass index" (BMI) have probabilistic causal effect on "heart disease"?
  - Intuition: there are different ways to change BMI, and these might have different effects on heart disease
  - Our strategy: clarify what we mean by "variables" and "effects", then use clarifications to examine "causal effects"

We need to understand what we mean by "variable"
  - Complex because variables have two jobs: (1) well-defined elements of mathematical models and (2) indicate which parts of the world are being modelled
  - (2) imposes some constraints, so we propose: require that models are compatibile with variables
   - Result: Compatibility is equivalent to the standard approach to probability modelling + "strict compaitibility of conditionals"
  - Definition: A model is a Markov kernel + an index that satisfies compatibility
  - Plus we need a bunch of mathematical tools (string diagrams, conditional probability, conditional independence, consistent extension)

What do *we* mean by "effect"?
  - Motivation: We have a decision to make. To select one of the choices, we compare consequences
    - I.e. *choices* are necessarily paired with consequences, not so arbitrary variables
  - Working hypothesis: "causal effects" of arbitrary variables are underpinned by consequences
  - We introduce see-do models, which model consequences in a class of decision problems with inference
    - Result: classical statistical decision theory is a special case of see-do model + expected utility

How are causal effects related to consequences in Causal Bayesian Networks?
  - CBN do not have different variables to represent observations and consequences, but constraints imply they must be represented by different variables
  - Proposal: a CBN provides two probabilistic models, which can be "tethered" n times to create full model of observations and effects
    - Analogous to representing a conditionally IID model with a single point probability distribution, which can be "tethered" n times to generate the entire model
  - The "CBN model" is a see-do shaped Markov kernel, but it's only a see-do *model* if it also has the right index
    - Result: A CBN model can be extended to a properly indexed see-do when "intervenables" are proxies for decisions (conditional independence condition)
  - Proposal: variables have causal effects when they are proxies for decisions

How are causal effects related to consequences in Potential Outcomes models?
  - Just like CBN, potential outcomes models do not include variables that represent consequences of decision, and we need them
  - Proposal: potential outcomes represent consequences via conditional IID assumption
  - The resulting "PO model" is a see-do shaped Markov kernel
    - As with CBN, can be extended to a see-do model if selection variables are proxies for decisions

  - What about defining causal effects via counterfactuals instead of consequences?
    - Result (in appendix): potential outcomes representation of sequence of (decision, conseqeunce) iff (decision, conseqeunce) are exchangeable + deterministically repeatable
      - Assumption of exchangeable + deterministically repeatable is explicit in result, only implicit in "counterfactual" account of potential outcomes
      - Even in idealised experiments, these assumptions don't hold if selection variable does not proxy for actions

  - Proposal: variables induce potential outcomes when they are proxies for decisions


Conclusion
  - There is a lot of interest in learning causes from data (i.e. how see-do models should be constructed), which we don't address here
  - If you want to know how to learn something, it helps to be clear about what you are learning
  - Future work:
    - Approximate version of "variable is a proxy for decision" assumption
    - Inductive hypotheses
    - How do I know my variable is a proxy for your decision?