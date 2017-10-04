# Sanskrit compound segmentation using seq2seq model 
Code for the paper titled 'Building a Word Segmenter for Sanskrit Overnight'

Instructions
============

Pre-requisites
--------------
The following python packages are required to be installed:
* Tensorflow: https://www.tensorflow.org/, tensorflow version 0.12.1 was used for this project. 

File organization
-------------------------------------------
* Data is located in data/.
* Logs generated by tensorflow summarywriter is stored in logs/.
* Models which are trained are stored in models/.

Training
--------
The file train.py can be used to train the model.
The file test.py can be used to test the model.

Data
-------------------------------------------
data/ folder contains all the data used for the segmentation task.

All the .txt files are already tokenized using sentencepiece, the m.vocab and m.model files are the onces generated by sentencepiece and they can be used to tokenize any other data with the same vocabulary.

All .txt files contain data which are separeted by a new line(\n).

### Training data: 
* dcs_data_input_train_sent.txt file contains the input sentences used for training. 
* dcs_data_output_train_sent.txt file contains the output words(segmented forms of input) used for training.

### Testing data: 
* dcs_data_input_test_sent.txt file contains the input sentences used for testing. 
* dcs_data_output_test_sent.txt file contains the output words(segmented forms of input) used for testing.

Once the train.py file is run, it creates various other files for word2id, id2word, ... more details are provided in the utils/data_loader.py file.
