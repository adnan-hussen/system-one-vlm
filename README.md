# system-one-vlm

This notebook implements a decision or "system one" model by removing autoregressive generation from a Qwen 3.5 model with 2 billion parameters. The output can be of type "noul", "choice", or "score", allowing the model to provide deterministic answers with low latency (average of 300ms on Tesla T4 GPU). These outputs are the result of taking the softmax of the scores of the words relevant to the decision from the unembedding matrix of the LLM.
