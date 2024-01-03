# SCAN_Replication

I have replicated the LSTM architecture described by Lake and Baroni and I have replicated the experiments written in their [paper](https://github.com/MatiasSalaris/SCAN_Replication/blob/main/Paper.pdf)https://github.com/MatiasSalaris/SCAN_Replication/blob/main/Paper.pdf 

The general idea was to train a network to associate to a compositional navigation command sentence, the correspective sequence of actions.
For example, receiving as input the sentence:
"Jump Left"
The expected output is:
"LTURN JUMP".

While a more complicated one could be:
"Jump opposite left after walk around left"  -> "LTURN WALK LTURN WALK LTURN WALK LTURN WALK
LTURN LTURN JUMP"
