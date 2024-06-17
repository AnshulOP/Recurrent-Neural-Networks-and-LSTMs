                      Recurrent Neural Networks (RNNs): Architecture and Working
                      
RNNs are a special kind of neural network designed to handle sequential data, such as time series data, text, or speech. Unlike traditional neural networks where each layer operates independently, RNNs have internal connections that allow them to process information from previous steps in the sequence. This "memory" capability makes them powerful tools for tasks like language translation, speech recognition, and time series forecasting.

### Basic Architecture
An RNN can be visualized as a loop or chain of interconnected processing units. Here's a breakdown of the key components:

**Input Layer:** Receives the data at each time step. For example, in a sentence, each word would be an input vector.

**Hidden Layer:** The heart of the RNN. It contains a set of interconnected nodes that process information and maintain a hidden state. This hidden state acts as the network's memory, capturing information from previous inputs. The same set of weights are shared across all hidden layer nodes at different time steps.

**Output Layer:** Generates the output for each time step. This could be a classification (e.g., identifying the part of speech for a word) or a prediction (e.g., the next word in a sentence).

### Working of RNNs
Here's how information flows through an RNN:

**Initialization:** The hidden state (h) is initialized with zeros or some other starting value.

**Input & Hidden Layer Interaction:** At each time step (t), the current input (x(t)) is fed into the network along with the previous hidden state (h(t-1)).

**Activation Function:** The combined input (x(t) and h(t-1)) is passed through an activation function (e.g., sigmoid or tanh) to introduce non-linearity and transform the data.

**Hidden State Update:** The output from the activation function is used to update the hidden state (h(t)). This update involves weights (W) that determine how much influence the current input and previous hidden state have on the new hidden state.

**Output Generation:** The updated hidden state (h(t)) is used to generate the output (y(t)) for the current time step. This may also involve additional weights and an activation function.

**Looping:** Steps 2-5 are repeated for each element in the sequence. The updated hidden state from the previous step becomes the input for the current step, allowing the network to learn long-term dependencies within the sequence.

**Key Point:** Sharing weights across all time steps allows the RNN to learn a single set of parameters that can be applied to any sequence length. This is efficient but can lead to limitations, discussed later.

### Backpropagation Through Time (BPTT)
Training RNNs involves adjusting the weights based on the difference between the predicted and actual outputs. This process is called backpropagation. However, in RNNs, the output at a given time step depends on all previous inputs and hidden states. To address this, a modified version of backpropagation called Backpropagation Through Time (BPTT) is used. BPTT unfolds the RNN across time steps, essentially creating a much deeper network. It then calculates the gradients for each weight considering its influence on all subsequent outputs.
