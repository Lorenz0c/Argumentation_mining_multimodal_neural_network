# Argumentation_mining_multimodal_neural_network

The process konwn as Argumentation mining consist in the automatic extraction of the argumentative structure contained in a text.
There are many possible variants of this process.
The one here adressed requires to perform three main step in order to achive the desired result.
The first step consist in the identification of the limits of each argumentative section contained in the text.
The second step to perform consists in the separation between these sections between premises and claims.
The third and last step consist in the extraction of the relations which connect the different argumentative sections.

This process is very complex and time consuming even for humans.
Many researches have tried to address this problem with the use of machine learning techniques. 

The main objective of the work here executed was to try to analyse if and how different types of structured data, extracted from the texts, can be usefull in the learning process with respect to the unstructured data consisting in the sequences of words which compose the texts considered.
The types of structured data to use for each of the three steps to perform have been extracted and selected in the scripts contained in the "preprocessing" folder.
The STC (Sparse Tensor Classifier) has been used to decect which types of data contained more information and which contained mostly noise, for each one of the three steps to perform.
The folders contained in the preprocessing one have been numered to indicate the order in which they have to be performed.

Once concluded the preprocessing steps, different multimodal neural networks have been trained to combine different types of structured data with the unstructured data obtained from the texts.
Each combination of structured data considered has also been used to train a feed-forward neural network without the use of the unstructured data, in order to analyze also the importance of this last type of data in the learning process.

Once the learning phase have been executed, some of the neural networks trained have been chosed as representative for each one of the three steps.
The elements of the test set used to evalue the results of the learning have been labeled with the result of the predictions perfomed by each of the selected networks (false positive, false negative, ecc...).
The STC has than be used to try analyze the errors and to try to find out which of the types of structured data considered could lead to furder improvements in each of the network choosed.

Three dataset for argumentation mininghave been used: the Argument Annotated Essays Corpus (v2.0), the IBM Debater - Claim and sentences and the arg-microtexts corpus.
In onrder to learn to predict a subjectivity score for each sentence in the corpus another dataset has been used: the subjectivity dataset v1.0.
