### generatively pre-trained transformer (GPT) - part 1

- Attention is all you need - https://arxiv.org/pdf/1706.03762.pdf
- single self attention head - is a linear layer with 3 weight matrices - query, key, value
- https://youtu.be/5vcj8kSwBCY?list=PLaPdEEY26UXyE3UchW0C742xh542yh0yI
- what is self attention vs cross attention - self attention is when the query, key, value are all from the same sentence, cross attention is when the query is from one sentence and the key and value are from another sentence
- softmax function - it is a function that takes a vector and returns a vector of the same size with values between 0 and 1 and the sum of the values is 1
- register_buffer - it is a way to register a tensor as a buffer - buffers are tensors that are not used in the forward pass but are used in the backward pass?
- deep residual learning for image recognition - https://arxiv.org/pdf/1512.03385.pdf
- skip connections - they are connections that are added to the output of a layer and added to the input of the next layer - residual connections are a type of skip connection
- skip connection are forked off - add the desired code in the forward pass 
- projection layer for residual connection - it is a linear layer that is used to project the input to the same size as the output of the residual connection
- layernorm - it is a normalisation technique that is used to normalise the data - it is used to normalise the data to have a mean of 0 and a std of 1
- what is the difference between batchnorm and layernorm? - batchnorm is used to normalise the data across the batch dimension, layernorm is used to normalise the data across the feature dimension
- pre norm vs post norm - pre norm is when the normalisation is done before the activation function, post norm is when the normalisation is done after the activation function
- decoder only transformer
- what is encoder and decoder - 
- dropout paper - find the archive link - 
- for different iterations of forward and backward pass, the dropout mask is different, hence it ends up training an ensemble of networks
- cross attention block takes in encoder input? and adds it in the decoder block
- traingular mask on top of the attention matrix - it is used to mask the attention matrix so that the decoder can only attend to the previous words and not the future words
- autoregressuve meaning - it is when the model predicts the next word based on the previous words
- in attention is all you need - they conditioned the decoding not only on the past of the decoding input but also in the encoder input 
- gelu - it is a non linear activation function - it is a smooth approximation of relu
- gpt3 paper - https://arxiv.org/pdf/2005.14165.pdf - language odels are few shot learners
- after training gpt model, it goes through an alignment step