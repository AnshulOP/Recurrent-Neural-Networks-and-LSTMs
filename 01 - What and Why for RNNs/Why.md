## Why RNNs were required:
Recurrent Neural Networks (RNNs) were developed to address the limitations of traditional Artificial Neural Networks (ANNs) in handling sequential data. ANNs, while powerful for many tasks, lacked the ability to effectively model sequences because they treated each input independently, without considering the order or relationship between inputs.

## Why ANNs were not used:
ANNs were not well-suited for sequential data because they lacked memory. In an ANN, each input is processed independently, and there is no inherent mechanism to retain information about previous inputs. This means ANNs struggle with tasks where the order of the inputs matters, such as time series prediction, language modeling, and speech recognition.

## How ANNs used to work:
ANNs consist of layers of interconnected nodes, where each node performs a simple computation on its input and passes the result to the next layer. In a typical feedforward ANN, information flows in one direction, from input to output, with no feedback loops or memory of past inputs.

## How RNNs work differently:
RNNs, on the other hand, are designed to handle sequential data by introducing loops within the network, allowing information to persist over time. Each node in an RNN receives input not only from the current time step but also from the previous time step, effectively giving the network a form of memory. This allows RNNs to capture temporal dependencies in data.

## Example approach:
Let's consider the task of predicting the next word in a sentence. In an ANN, each word would be treated as an independent input, and the network would have no awareness of the order of the words. However, in an RNN, the network maintains a hidden state that is updated at each time step, incorporating information from previous words. This hidden state serves as a form of memory, allowing the network to consider the context of the entire sentence when making predictions.

For instance, in the sentence "The cat is chasing the...", an ANN might struggle to predict the next word without considering the preceding words. However, an RNN would use its memory of the previous words to predict that the next word is likely to be something related to the action of "chasing", such as "mouse" or "bird".

In summary, RNNs were required to address the limitations of ANNs in handling sequential data by introducing memory mechanisms that allow them to capture temporal dependencies and process sequences effectively.
