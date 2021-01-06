## This project trains a feed-forward neural network to predict the transitions of a dependency parser.

#### conll_reader.py - data structures to represent a dependency tree, as well as functionality to read and write trees
#### get_vocab.py = extract a set of words and part of speech tags that appear in training data
#### extract_training_data.py - extracts two numpy matrices representing input output pairs
#### train_model.py - build and train model
#### decoder.py - use model to parse input
#### evaluate.py - use input dependencies to compare parser output

### Data files are from WSJ part of Penn Treebank

#### Obtain vocab - `python get_vocab.py data/train.conll data/words.vocab data/pos.vocab`
#### Train model - `python train_model.py data/input_train.npy data/target_train.npy data/model.h5`
#### Build parser - `python decoder.py data/model.h5 data/dev.conll`
#### Evaluate parser - `python evaluate.py data/model.h5 data/dev.conll`


