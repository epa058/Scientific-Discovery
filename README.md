# Machine Learning for Scientific Discovery

This project explores the use of machine learning as a tool for scientific discovery.

Machine learning is typically used to recognize patterns, make predictions, or approximate solutions to problems for which we already understand the underlying rules. A more ambitious possibility is to use learning algorithms to discover the rules themselves: given some data, can a model identify the underlying structure of the system that generated it? In particular, can machine learning move beyond fitting experimental data and recover meaningful representations of physical laws from observations? Ultimately, I am interested in whether sufficiently capable learning algorithms could be used not merely to reproduce known physical theories, but to help discover the mathematical structure underlying experimental observations.

**Maybe Yes:** There are examples suggesting that neural networks can learn internal representations that go beyond simple surface-level pattern matching. In the Othello-GPT experiment [1](https://thegradient.pub/othello/), for example, a language model was trained only on sequences of moves, without being given the rules or board state of the game. The resulting model nevertheless developed internal representations that corresponded to the state of the Othello board.

**Maybe no:** At the same time, good predictive performance does not necessarily mean that a model has discovered the underlying rules of a system. Recent work studying models trained on orbital trajectories found that models could perform their training tasks while failing to generalize according to Newtonian mechanics [2](https://arxiv.org/abs/2507.06952). This highlights an important distinction between learning to merely predict data versus discovering the rules that generate the data.

## A Toy Experiment

Before applying these ideas to physical systems, it is useful to study them in a much simpler setting.A Transformer trained only on English text can learn a substantial amount of the statistical structure underlying English without being explicitly given a grammar book. The important distinction, though, is learning to predict English vs. discovering the rules of English. A Transformer can become extremely good at predicting the next token while relying partly on statistical correlations rather than representing an explicit grammatical rule. However, for example, it can be difficult to determine whether it has learned the abstract rule of subject–verb agreement.

I'm not actually sure how to implement this English example, so I'm working with binary sequences instead. 

## FAQ

**Q: What is ``PatternRecognition1?``**

**A:** ``PatternRecognition1`` was an idea I first heard from my supervisor in 2024, and I had wanted to implement it since then. It basically asks whether a Transformer can detect structure in human-generated binary sequences that are intended to be random. Turns out a similar experiment already exists [3](https://github.com/DragonDmoney/HumanRandomness), but it was still pretty cool to build it independently. I didn't really mention it above because it's kind of a tangent to the main scientific discovery idea.

## References

* **Othello-GPT:** [Do Large Language Models learn world models or just surface statistics?](https://thegradient.pub/othello/)
* **World models and orbital mechanics:** Vafa et al., *What Has a Foundation Model Found? Using Inductive Bias to Probe for World Models*, [arXiv:2507.06952](https://arxiv.org/abs/2507.06952)
* **Human randomness:** [DragonDmoney/HumanRandomness](https://github.com/DragonDmoney/HumanRandomness)
