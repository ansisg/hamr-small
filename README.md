Copy of https://github.com/ansisg/hamr/, optimized to a browser friendlier size (285MB -> 50MB) <br/>
<br/>
Training: <br/>
100M links from commoncrawl (https://commoncrawl.org/url-index) <br/>
500K links from reddit outbound links dataset, manually adjusted to reduce biases (https://github.com/smythp/reddit_links_dataset) <br/>
Tokenized into a 8k vocabulary using SentencePiece (https://github.com/google/sentencepiece) <br/>
Training data is preprocessed into tokens and dumped in one file separated by EOS, random segments sampled during training <br/>
~3.4B tokens total training data <br/>
Model: <br/>
Llama style GPT, SwiGLU and RMSNorm, Rotary embeddings <br/>
8 layers, 8 heads, 192 hidden dim, 256 context window <br/>
Trained for 5B tokens total (basically fully trained by then) <br/>
Exported into .onnx for browser use <br/>
