# confirmation_bias_illusory_truth

Includes PDFs of early drafts along with sample code.

This model investigates the effects of confirmation bias in conjunction with illusory truth on agents’s ability to successfully form a consensus about the truth. The type of confirmation bias investigated (Hart et al. 2009) involves agents being less likely to update their beliefs based on evidence that they know disagrees with their prior beliefs. Extending a model from Zollman \cite{zollman_2010}, I have already explored confirmation bias with results showing that a moderate amount of confirmation bias can benefit group learning. However, one can still question how robust this result is. Here I propose investigating confirmation bias with the addition of an illusory truth dynamic. Illusory truth (Fazio 2020, (Pennycook et al. 2017, Dechêne et al. 2009) is a phenomenon in which an agent's credence in a statement increases with repeated exposure to that statement, even in cases in which the statement is a known falsehood. It is also easy to conceive of natural ways in which one might be repeatedly exposed to the same claim or piece of evidence; perhaps a particular journal article is often discussed in ones social circle. If some data points are allowed to persist in an epistemic network, then can moderate confirmation bias lead to stable polarization of beliefs? Initial simulation results show that the combined dynamic can substantially lower the success rates of networks, but have yet to yield stable polarization.

As in the previous model, confirmation bias is captured in an agent's probability of accepting the results of others; this probability is determined by the agent's prior beliefs about the probability of the shared results obtaining. As the probability of the results decreases, the probability that the agent will accept the shared results and update her beliefs also decreases. Illusory truth is modeled as agent's having a memory of $M$ many data points previously accepted, randomly sharing $S$ many of those data points on each round, and randomly choosing at most $D$ many data points in memory to be replace by newly accepted data points. 

Networks are evaluated based on the rate of successful convergence to true beliefs for a fixed set of parameters. Parameters that are varied across simulations are: network size, network structure, objective probability of success for each bandit arm, number of pulls per round, tolerance, $t$, memory size, $M$, amount of old data shared, $S$, and amount of new data saved to memory $D$. In a possible variation on the model, I may consider a dynamic in which agents always save to and share from memory the data points that most agrees with their prior beliefs, rather than randomly selecting data.