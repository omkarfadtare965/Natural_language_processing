- RNN stands for Recurrent Neural Network, which is a type of neural network especially useful when working with sequential data.
-
-
-
- Sequential data is data where the order matters, and each piece of data depends on the previous ones. Examples include textual sentences, audio, video, stock prices, etc. On the other hand, non-sequential data is data where the order doesn’t matter. Each piece of data is independent of the others. Examples include images, customer names, etc.
- ANNs (Artificial Neural Networks) can't be used effectively for making predictions on sequential data because they process each input independently without remembering previous inputs. This means ANNs can't handle tasks where past inputs influence the current output (e.g., predicting the next word in a sentence based on previous words). In contrast, RNNs can remember inputs from previous steps, which allows them to make predictions based not only on the current input but also on what has been seen before. This ability to "remember" helps RNNs understand sequences where past information is critical for making accurate decisions.
- Each hidden state of an RNN captures information about the previous inputs, which is passed forward through the network, making them good at modeling time-dependent or sequential data.



Applications of RNNs: 
- Time series forecasting
- Natural language processing (NLP)
- Speech recognition
- Video analysis




Hidden state
- The hidden state in an RNN  is a representation that holds the memory of the information from previous time steps in the sequence. It’s like a "summary" or "memory" that the RNN carries forward as it processes each step in the sequence.
Imagine you're reading a sentence word by word. The hidden state works like your brain’s memory, storing the words you’ve already read so that you can understand the whole sentence as you move forward.
it acts like a bridge, connecting the past information with the current processing.
For each time step, the hidden state is updated based on:

The current input at that time step.
The previous hidden state

Forward Propagation: For each time step, the input is combined with the hidden state from the previous time step. This combination is processed through activation functions to produce the output and update the hidden state.

Backward Propagation (BPTT - Backpropagation Through Time): RNNs use backpropagation to minimize the loss function. However, they do this by unrolling the network through time and calculating gradients for each time step. This process is called "unfolding through time" and allows the RNN to adjust weights based on how much the current input influences outputs at future time steps.

Unfolding Through Time
Hidden state
return_sequence=False
Types of RNN and its example
What is timesteps
How to decide number of  timesteps?
