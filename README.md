# Survey-of-Transformer-Architecture-Search

This is a summary of Neural Architecture Search (NAS) on Transformer, named TAS.
## Summary of TAS
| Category 	| Task 	| Method 	| Search Space      (3-level: Hyperparameter-level, Module-level, Architecture-level) 	| Search Strategy   & Performance Estimation 	| Publication 	|
|:---:	|:---:	|:---:	|:---:	|:---:	|:---:	|
| Natural Language      Processing 	| Improving Performace 	| Auto-Sizing  Transformer 	| H-level:   Auto reducing the size of model in training 	| Gradient optimization   & Train a supermodel  	| arxiv 2019-10 	|
|  	|  	| SandWich Transformer 	| A-level: The permutation (order) of FFN and Self-Attention 	| Random search & Sample solutions, train and   evaluate them 	| arxiv 2020-4 	|
|  	|  	| Multi-Pass Transformer 	| A-level: information flow in   Encoders      (1. multi-pass encoder 2. information flow between these encoders) 	| Random search & Sample solutions, train and   evaluate them 	| arxiv 2020-9 	|
|  	|  	| 　 	| 　 	| 　 	| 　 	|
|  	|  	| Evolved Transformer 	| M-level: cell search space 	| EA &   Sample solutions, train them with early stopping   for their evaluation 	| arxiv 2017 	|
|  	|  	| AutoTrans 	| M-level: 1.cell search space   2.activation 3.Norm      4.heads number 5.relative dimension 	| RL   & Sample solutions in a   supermodel       (one-shot method) 	| arxiv 2020-9 	|
|  	|  	| 　 	| 　 	| 　 	| 　 	|
|  	|  	| CAS(Language Models with Transformers) 	| M-level: Modification:   1.AddLinear      2.AddLSTM 3.FixSubset  	|  Coordinate architecture search & Sample solution, fine-tune   and evaluate them 	| arxiv 2019-10 	|
|  	|  	| 　 	| 　 	| 　 	| 　 	|
|  	|  	| 　 	| 　 	| 　 	| 　 	|
|  	|  	| NAS-BERT 	| M-level: 1.Embedding Size 2.heads   number       3.Hidden Size 4. SepConv 3 5 7       5. Identity 	| Direct   sample (selection) &   Sample solutions in a supermodel       (one-shot method) and performance approximation 	| arixv 2021-5 	|
|  	|  	| AdaBert 	| 　 	| 　 	| arxiv 2021-1 	|
|  	|  	| AutoBERT-Zero 	| 　 	| 　 	| arxiv 2021-7 	|
|  	|  	| Length-Adaptive Transformer 	| 　 	| 　 	| arxiv 2021-6 	|
|  	|  	| 　 	| 　 	| 　 	| 　 	|
|  	|  	| 　 	| 　 	| 　 	| 　 	|
|  	| Hardware-aware       Deployment 	|  Fast Transformers 	| M-level:1.Dimension of Q K V 2.   heads number      3. LN mean value 4. Width of depth of FFN  	| Sampling   distribution optimization &   Sample solutions in a supermodel       (one-shot method) 	| arxiv 2020-8 	|
|  	|  	| HAT 	| M-level: 1. Layer num in   encoder/decoder      2. Dimension of embedding, hidden layer in FFN and  heads number      3.Arbitrary encoder-decoder attention (Link)  	| EA   & Sample solutions in a supermodel (one-shot method)      and surrogate hareware predictor 	| arxiv 2020-5 	|
|  	|  	| RankNAS 	| M-level: 1. Layer num in   encoder/decoder      2. Dimension of embedding, hidden layer in FFN and  heads number      3.Arbitrary encoder-decoder attention (Link)       ---------------------Extra to HAT ---------------      4. Norm type(Pre-LN, Post-LN)      5.RPR Len [8,12,16] ( the maximum relative position Representations) 	| Random   search/EA & Sample   solutions in a supermodel (one-shot method)       and rank and select them by the  ranking model 	| arxiv 2021-9 	|
|  	|  	| DARTsFormer 	| M-level: •  Standard Conv w × 1: for w in 3, 5, 7,   11.      • Dynamic Conv w × 1: for w in 3, 7, 11, 15.      • Self Attention; • FFN.      • Cross Attention: Only available to decoder.      • Gated Linear Unit (GLU).      • Zero: Return a zero tensor of the input size.      • Identity: Return the input. 	| Gradient   optimization (Multi-split reversible network for reducing memory)      & Train a   supermodel  	| arxiv 2021-5 	|
|  	|  	| 　 	| 　 	| 　 	| 　 	|
|  	|  	| 　 	| 　 	| 　 	| 　 	|
|  	|  	| 　 	| 　 	| 　 	| 　 	|
|  	| Quantization 	| Mixed Precision   Quantization Transformer 	| H-level:   1-bit, 2-bit, 4-bit and 8-bit 	| Gradient optimization   & Train a supermodel  	|  ICASSP 2021 	|
|  	| Other 	| TextNAS 	| Not Transformer: 1. Convolutional Layers      2.Recurrent Layers 3.Pooling Layers      4.Multi-Head Self-Attention Layers 	| RL   same as ENAS & Sample   solutions in a supermodel       (one-shot method) 	| AAAI 2020 	|
|  	|  	| 　 	| 　 	| 　 	| 　 	|
| Computer       Vision 	| 　 	| AutoFormer 	| 　 	| 　 	| arxiv 2021-7 (ICCV) 	|
|  	| 　 	| GLiT 	| 　 	| 　 	| arxiv 2021-8 	|
|  	| Multi-stage 	| Vit-ResNAS 	| 　 	| 　 	| arxiv 2021-9 	|
|  	| 　 	| PSViT 	| 　 	| 　 	| arxiv 2021-8 	|
|  	| 　 	| 　 	| 　 	| 　 	| 　 	|
|  	| 　 	| 　 	| 　 	| 　 	| 　 	|
|  	| 　 	| 　 	| 　 	| 　 	| 　 	|
|  	| Vanilla NAS for CNN 	| NAT (not search for   Transformer) 	| 　 	| 　 	| PAMI 2021  	|
|  	| 　 	| 　 	| 　 	| 　 	| 　 	|
| Speech 	| Speech   Recognition 	| Evolved   Speech-Transformer 	| M-level:   cell space (same as Evolved Transformer)  	| EA   & Sample solutions   and  progressive dynamic hurdles (early   stopping) 	| INTERSPEECH 2020 	|
|  	|  	| Streaming Transformer 	| 　 	| 　 	| arxiv 2020-11 	|
|  	| 　 	| 　 	| 　 	| 　 	| 　 	|
| Other 	| 　 	| 　 	| 　 	| 　 	| 　 	|
|  	| 　 	| 　 	| 　 	| 　 	| 　 	|
|  	| 　 	| 　 	| 　 	| 　 	| 　 	|
