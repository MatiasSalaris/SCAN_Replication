## SCAN_Replication

I have replicated the LSTM architecture described by Lake and Baroni and I have replicated the experiments written in their [paper](https://github.com/MatiasSalaris/SCAN_Replication/blob/main/Paper.pdf)https://github.com/MatiasSalaris/SCAN_Replication/blob/main/Paper.pdf 

The general idea was to train a network to associate a compositional navigation command sentence to the respective sequence of actions through supervised learning.
This was done using a simplified Natural Language called SCAN, which contains a limited amount of input words and a corresponding amount of output ones.
For example, a simple input sentence could be:

"Jump Left"

And its expected output:

"LTURN JUMP".

While a more complicated one could be:

"Jump opposite left after walk around left"  -> "LTURN WALK LTURN WALK LTURN WALK LTURN WALK
LTURN LTURN JUMP"

---


# Experiments

The model was also trained and evaluated on the 3 experiments described in the paper, achieving overall similar results.
<br />
<br />


*Experiment 1*

The first experiment consisted of training the model with small portions of training data in order to test its ability to generalize.
<br />
<br />
<br />

*Experiment 2*

The second experiment consisted of training the model on the full training data, but evaluating it on sentences exceeding the length of any previously seen input.
<br />
<br />
<br />

*Experiment 3*

The third experiment consisted of adding some words such as "run" to the vocabulary, showing them to the model as stand-alone primitives during training, and then evaluating the ability of the model to generalize the composition of these new words and the rest of the known vocabulary.
To have a better visual explanation:
The model would learn from all the training data seen in the previous experiments, plus various instances of the primitive:

"run" with the corresponding output "RUN".


But during evaluation it would come across input sentences such as:

"turn left after run twice"



