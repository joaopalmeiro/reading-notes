# MIT 6.S191: Introduction to Deep Learning

> [Website](http://introtodeeplearning.com/).

## Lecture 1: Intro to Deep Learning

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

## Lecture 2: Deep Sequence Modeling

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
