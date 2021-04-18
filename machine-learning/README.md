- [Courses](#courses)
  - [MIT 6.S191: Introduction to Deep Learning](#mit-6s191-introduction-to-deep-learning)
- [Papers/Articles](#papersarticles)
  - [`The Hardware Lottery`](#p1)
- [Talks](#talks)
  - [`Machine Learning Performance Monitoring`](#t1)

## Courses

### MIT 6.S191: Introduction to Deep Learning

[Website](http://introtodeeplearning.com/).

#### Lecture 1: Intro to Deep Learning

- Deep Learning: extract patterns/features from (raw) data using neural networks.
- "The key idea of Deep Learning is to learn these features directly from data in a hierarchical manner."
- Bias term: "(...) allows you to shift your activation function left or right."
- "The purpose of activation functions is to introduce non-linearities into the network". "(...) allows us to actually deal with non-linear data."
- "Linear activation functions produce linear decisions no matter the network size".
- Perceptron (3 steps):
  1. Dot product of inputs and weights.
  2. Add a bias.
  3. Apply non-linearity.
- Fully-connected layer or dense layer.
- Empirical loss, objective function, cost function, or empirical risk. It "(...) measures the total loss over our entire dataset".
- Loss optimization: "We want to find the network weights that achieve the lowest loss".
- Gradient descent:
  - "The gradient tells us the direction of highest or steepest ascent (...) tells us which way is up."
  - "Take a small step in the opposite direction of gradient".
- "Computing the gradient of our loss $J(W)$ with respect to one of the weights, in this case just $W_2$, (...) tells us how much a small change in $W_2$ is going to affect our loss $J(W)$."
- Learning rate:
  - "(...) tells us how large should each step we take in practice be with regards to that gradient."
  - "Small learning rate converges slowly and gets stuck in false local minima".
  - "Large learning rates overshoot, become unstable and diverge".
  - "Stable learning rates converge smoothly and avoid local minima".
  - Adaptive learning rates: "Learning rates are no longer fixed".
- "The gradient tells us the direction but it doesn't necessarily tell us the magnitude of the direction. So, the learning rate can tell us actually a scale of how much we want to trust that gradient and step in the direction of that gradient."
- Stochastic gradient descent:
  - "Pick single data point $i$".
  - "Easy to compute but very noisy (stochastic)".
  - Middle ground: "Pick batch of $B$ data points".
- Regularization:
  - "Technique that constrains our optimization problem to discourage complex models".
  - Dropout:
    - "During training, randomly set some activations to 0".
    - "Forces network to not rely on any 1 node".

#### Lecture 2: Deep Sequence Modeling

- Applications:
  - "One to One: Binary Classification". "(...) from a static input to a static output".
  - "Many to One: Sentiment Classification".
  - "One to Many: Image Captioning".
  - "Many to Many: Machine Translation".
- "Neurons with Recurrence". The output will depend not only on the input but also on the past memory. "The cell state (...) depends on the current input and (...) on the prior cell states."
- "RNNs have a state, $h_t$, that is updated at each time step as a sequence is processed".
- "Re-use the same weight matrices at every time step".
- To model sequences (design criteria):
  1. "Handle variable-length sequences".
  2. "Track long-term dependencies".
  3. "Maintain information about order".
  4. "Share parameters across the sequence". "(...) we can achieve both points 2 and 3 by using weight sharing (...)".
- "Embedding: transform indexes [(a set of identifiers for objects)] into a vector of fixed size."
- Backpropagation:
  1. "Take the derivative (gradient) of the loss with respect to each parameter".
  2. "Shift parameters \[(weights)\] in order to minimize loss".
- "Why are vanishing gradients a problem?"
  - "Multiply many small numbers together".
  - "Errors due to further back time steps have smaller and smaller gradients".
  - "Bias parameters to capture short-term dependencies".
- LSTMs:
  - "LSTM modules contain computational blocks that control information flow".
  - "Information is added or removed through structures called gates".
  - "Gates optionally let information through, for example via a sigmoid neural net layer and pointwise multiplication". "(...) because we have the sigmoid activation function, this is going to force anything that passes through that gate to be between 0 and 1. So, you can (...) think of this as modulating and capturing how much of the input should be passed through — between nothing, 0, or everything, 1 (...)".
  - "Maintain a separate cell state from what is outputted ($c_t$)".
  - "(...) it's really this maintenance of the separate cell state $c_t$ which allows for backpropagation through time with uninterrupted gradient flow (...)".
- "How do LSTMs work?"
  1. "Forget". "LSTMs forget irrelevant parts of the previous state".
  2. "Store". "LSTMs store relevant new information [(from current input)] into the cell state".
  3. "Update". "LSTMs selectively update cell state values". "(...) by these gatewise operations".
  4. "Output". "The output gate controls what information is sent to the next time step". In other words, "Output gate returns a filtered version of the cell state".
- "Attention mechanisms (...) provide learnable memory access".

---

## Papers

The (bullet point) text enclosed in double quotation marks refers to quotes from the author(s) of the respective paper.

---

### P1

[`The Hardware Lottery`](https://arxiv.org/abs/2009.06489) | Sara Hooker | 2020 | [Mind map](https://miro.com/app/board/o9J_kiSTlaI=/)

Monday, October 5, 2020

**Mind map**:

![Mind map for "The Hardware Lottery"](../assets/hw_lottery.jpg)

**Quotes, notes, and takeaways**:

- Note: This paper "(...) is part **position paper** and part **historical review**."
- **Hardware lottery**: "(...) when a research idea wins because it is suited to the available software and hardware and _not_ because the idea is superior to alternative research directions."
  - "In the field of artificial intelligence research, (...) it is our tooling which has played a disproportionate role in deciding what ideas succeed (and which fail)."
  - "(...) most computer science breakthroughs follow the Anna Karenina principle."
  - Anna Karenina principle: "(...) 'a deficiency in any one of a number of factors dooms an endeavor to failure.'"
- "(...) gains from progress in computing are likely to become even more **uneven**, with certain research directions moving into the fast-lane while progress on others is further obstructed."
- "After decades of treating hardware, software and algorithms as separate choices, the catalysts for closer collaboration include changing hardware economics (...), a 'bigger is better' race in the size of deep learning architectures (...) and the dizzying requirements of deploying machine learning to edge devices (...)."
- "Closer collaboration has centered on a wave of new generation hardware that is 'domain specific' to optimize for commercial use cases of deep neural networks (...)."
- "While domain specialization creates important efficiency gains for mainstream research focused on deep neural networks, it arguably makes it more even more costly to stray off of the beaten path of research ideas."
  - Domain-specific languages, self-tuning, hardware-aware programs, and profiling tools might help.
- "It is impossible to think of our cognitive intelligence without summoning up an image of the hardware it runs on [(brain)]."
- "Perhaps the **most salient example** of the damage caused by not winning the hardware lottery is the delayed recognition of **deep neural networks** as a promising direction of research [(Charles Babbage's Analytical Engine is another example)]."
  - "This gap between algorithmic advances and empirical success is in large part due to incompatible hardware."
  - "CPUs are very good at executing any set of complex instructions but incur high memory costs because of the need to cache intermediate results and process one instruction at a time [(von Neumann bottleneck)]."
  - von Neumann bottleneck:
    - "(...) the available compute is restricted by 'the lone channel between the CPU and memory along which data has to travel sequentially' (...)."
    - "(...) terribly ill-suited to matrix multiplies (...)."
- "It would take a hardware fluke [(an unexpected adaptation of GPUs)] in the early 2000s, a full four decades after the first paper about backpropagation was published, for the insight about massive parallelism to be operationalized in a useful way for connectionist deep neural networks."
- "The widespread and sustained popularity of symbolic approaches to AI cannot easily be seen as independent of how readily it fit into existing programming [(Lisp and Prolog)] and hardware frameworks."
- "To improve efficiency, there is a shift from task agnostic hardware like CPUs [(from the _general purpose era_ powered by Moore’s law and Dennard scaling)] to domain specialized hardware that tailor the design to make certain tasks more efficient."
- "Hardware is only economically viable if the lifetime of the use case lasts more than three years (...). Betting on ideas which have longevity is a key consideration for hardware developers. Thus, co-design effort has focused almost entirely on optimizing an older generation of models [(_traditional_ Deep Learning)] with known commercial use cases [(priority)]."
  - "There are also high risk efforts to explore the development of transistors using new materials (...)."
  - "The bottleneck will continue to be funding hardware for use cases that are not immediately commercially viable."
- "(...) specialized hardware makes sense if you think that future breakthroughs depend upon pairing deep neural networks with ever increasing amounts of data and computation."
- Comparison with the **brain**:
  - "Human brains despite their complexity remain extremely energy efficient. Our brain has over 85 billion neurons but runs on the energy equivalent of an electric shaver (...)."
  - "While algorithms like deep neural networks rely on global updates in order to learn a useful representation, our brains do not. Our own intelligence relies on decentralized local updates which surface a global signal in ways that are still not well understood (...)."
  - The brain needs far fewer labeled examples.
  - "(...) evidence suggests that the brain does not perform a full forward and backward pass for all inputs. Instead, the brain simulates what inputs are expected against incoming sensory data. Based upon the certainty of the match, the brain simply infills. What we see is largely virtual reality computed from memory (...)."

---

## Talks

### T1

[`Machine Learning Performance Monitoring`](https://youtu.be/iiLadbM_It8) | Emeli Dral | DataTalks.Club

Wednesday, March 31, 2021

**Notes**:

- Data drift: change in feature distribution.
- Concept drift: change in underlying relationships (same feature distribution, different target class distribution, for example).
- Gradual concept drift (model retraining can help) vs. sudden concept drift.
- Monitoring:
  - Service health (memory and latency, for example) vs. data health vs. model health.
  - Add ML metrics to service health monitoring (using Grafana for real-time models, for example) vs. prepare ML-focused reports/dashboards (for batch models, for example).
