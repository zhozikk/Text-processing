# Final Team Agera


#Introduction
Text Processing
We will work with unstructured data. In particular, we will work with text data to build a language model (LM).
LM is a probability distribution $p(\cdot)$ over sequence of words. For example, given text $T=(w_1\ w_2\ \dots \ w_{|T|})$, where $w_1,\ w_2\, \dots \ w_{|T|}$ is sequence of words and $|T|$ is the number of words in the sequence, LM assigns it probability as follows: $p(T)=p(w_1\ w_2\ \dots \ w_{|T|})$.
LM is employed in many applications such as automatic speech recognition (ASR), machine translation (MT), image captioning, text generation and so on. For example, LM is used in ASR to assess correctness of generated output transcripts.
Let's assume our ASR system generated two possible transcripts for some given speech signal: "recognize speech" and "wreck a nice beach". These two phrases sound similar, but the first one is more likely to be linguistically correct. We can use the probability of each transcript to determine the final output of ASR. The probabilistic model (LM) should assign a higher probability score to the correct answer.

#Background
We will use Penn Tree Bank (PTB) dataset as our text data in this assignment.Take a look at the PTB dataset. It is already pre-processed, i.e. words are tokenized, all letters are lowercased, numbers are replaced with the "N", some non-alphanumeric characters are removed and etc. We need to apply a few small changes for our assignment. Please note, only the most frequent 9,999 words are kept in the dataset, the rest of the words are replaced with the special <"unk>" symbol. This is done to reduce memory and computation requirements.The PTB dataset has been pre-processed. Nevertheles, let's learn some basic text pre-processing commands.
To lowercase a given string, you can use str.lower() command.

#Implementation
To build a probabilistic model of a text, we can employ the frequentist approach, i.e. use relative frequency to estimate probability scores. Suppose we want to estimate probability of a sentence "how are you", then we need to count how many times it appears in the dataset. This approach is infeasible for long and/or complex sentences that might be absent or appear a few times in the dataset.

