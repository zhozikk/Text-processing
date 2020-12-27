# Final Team Agera


Text Processing
We will work with unstructured data. In particular, we will work with text data to build a language model (LM).
LM is a probability distribution $p(\cdot)$ over sequence of words. For example, given text $T=(w_1\ w_2\ \dots \ w_{|T|})$, where $w_1,\ w_2\, \dots \ w_{|T|}$ is sequence of words and $|T|$ is the number of words in the sequence, LM assigns it probability as follows: $p(T)=p(w_1\ w_2\ \dots \ w_{|T|})$.
LM is employed in many applications such as automatic speech recognition (ASR), machine translation (MT), image captioning, text generation and so on. For example, LM is used in ASR to assess correctness of generated output transcripts.
Let's assume our ASR system generated two possible transcripts for some given speech signal: "recognize speech" and "wreck a nice beach". These two phrases sound similar, but the first one is more likely to be linguistically correct. We can use the probability of each transcript to determine the final output of ASR. The probabilistic model (LM) should assign a higher probability score to the correct answer:

We will use Penn Tree Bank (PTB) dataset as our text data in this assignment.
