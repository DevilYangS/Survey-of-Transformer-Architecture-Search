# Survey-of-Transformer-Architecture-Search

This is a summary of Neural Architecture Search (NAS) on Transformer, named TAS.
## Summary of TAS
<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-c3ow{border-color:inherit;text-align:center;vertical-align:top}
</style>
<table class="tg">
<thead>
  <tr>
    <th class="tg-c3ow">Category</th>
    <th class="tg-c3ow">Task</th>
    <th class="tg-c3ow">Method</th>
    <th class="tg-c3ow">Search Space<br>     (3-level: Hyperparameter-level, Module-level, Architecture-level)</th>
    <th class="tg-c3ow">Search Strategy   &amp; Performance Estimation</th>
    <th class="tg-c3ow">Publication</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-c3ow">Natural Language<br>     Processing</td>
    <td class="tg-c3ow">Improving Performace</td>
    <td class="tg-c3ow">Auto-Sizing  Transformer</td>
    <td class="tg-c3ow">H-level:   Auto reducing the size of model in training</td>
    <td class="tg-c3ow">Gradient optimization   &amp; Train a supermodel </td>
    <td class="tg-c3ow">arxiv 2019-10</td>
  </tr>
  <tr>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">SandWich Transformer</td>
    <td class="tg-c3ow">A-level: The permutation (order) of FFN and Self-Attention</td>
    <td class="tg-c3ow">Random search &amp; Sample solutions, train and   evaluate them</td>
    <td class="tg-c3ow">arxiv 2020-4</td>
  </tr>
  <tr>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">Multi-Pass Transformer</td>
    <td class="tg-c3ow">A-level: information flow in   Encoders<br>     (1. multi-pass encoder 2. information flow between these encoders)</td>
    <td class="tg-c3ow">Random search &amp; Sample solutions, train and   evaluate them</td>
    <td class="tg-c3ow">arxiv 2020-9</td>
  </tr>
  <tr>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
  </tr>
  <tr>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">Evolved Transformer</td>
    <td class="tg-c3ow">M-level: cell search space</td>
    <td class="tg-c3ow">EA &amp;   Sample solutions, train them with early stopping   for their evaluation</td>
    <td class="tg-c3ow">arxiv 2017</td>
  </tr>
  <tr>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">AutoTrans</td>
    <td class="tg-c3ow">M-level: 1.cell search space   2.activation 3.Norm<br>     4.heads number 5.relative dimension</td>
    <td class="tg-c3ow">RL   &amp; Sample solutions in a   supermodel <br>     (one-shot method)</td>
    <td class="tg-c3ow">arxiv 2020-9</td>
  </tr>
  <tr>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
  </tr>
  <tr>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">CAS(Language Models with Transformers)</td>
    <td class="tg-c3ow">M-level: Modification:   1.AddLinear<br>     2.AddLSTM 3.FixSubset </td>
    <td class="tg-c3ow"> Coordinate architecture search &amp; Sample solution, fine-tune   and evaluate them</td>
    <td class="tg-c3ow">arxiv 2019-10</td>
  </tr>
  <tr>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
  </tr>
  <tr>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
  </tr>
  <tr>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">NAS-BERT</td>
    <td class="tg-c3ow">M-level: 1.Embedding Size 2.heads   number <br>     3.Hidden Size 4. SepConv 3 5 7 <br>     5. Identity</td>
    <td class="tg-c3ow">Direct   sample (selection) &amp;   Sample solutions in a supermodel <br>     (one-shot method) and performance approximation</td>
    <td class="tg-c3ow">arixv 2021-5</td>
  </tr>
  <tr>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">AdaBert</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">arxiv 2021-1</td>
  </tr>
  <tr>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">AutoBERT-Zero</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">arxiv 2021-7</td>
  </tr>
  <tr>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">Length-Adaptive Transformer</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">arxiv 2021-6</td>
  </tr>
  <tr>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
  </tr>
  <tr>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
  </tr>
  <tr>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">Hardware-aware <br>     Deployment</td>
    <td class="tg-c3ow"> Fast Transformers</td>
    <td class="tg-c3ow">M-level:1.Dimension of Q K V 2.   heads number<br>     3. LN mean value 4. Width of depth of FFN </td>
    <td class="tg-c3ow">Sampling   distribution optimization &amp;   Sample solutions in a supermodel <br>     (one-shot method)</td>
    <td class="tg-c3ow">arxiv 2020-8</td>
  </tr>
  <tr>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">HAT</td>
    <td class="tg-c3ow">M-level: 1. Layer num in   encoder/decoder<br>     2. Dimension of embedding, hidden layer in FFN and  heads number<br>     3.Arbitrary encoder-decoder attention (Link) </td>
    <td class="tg-c3ow">EA   &amp; Sample solutions in a supermodel (one-shot method)<br>     and surrogate hareware predictor</td>
    <td class="tg-c3ow">arxiv 2020-5</td>
  </tr>
  <tr>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">RankNAS</td>
    <td class="tg-c3ow">M-level: 1. Layer num in   encoder/decoder<br>     2. Dimension of embedding, hidden layer in FFN and  heads number<br>     3.Arbitrary encoder-decoder attention (Link) <br>     ---------------------Extra to HAT ---------------<br>     4. Norm type(Pre-LN, Post-LN)<br>     5.RPR Len [8,12,16] ( the maximum relative position Representations)</td>
    <td class="tg-c3ow">Random   search/EA &amp; Sample   solutions in a supermodel (one-shot method)<br>      and rank and select them by the  ranking model</td>
    <td class="tg-c3ow">arxiv 2021-9</td>
  </tr>
  <tr>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">DARTsFormer</td>
    <td class="tg-c3ow">M-level: •  Standard Conv w × 1: for w in 3, 5, 7,   11.<br>     • Dynamic Conv w × 1: for w in 3, 7, 11, 15.<br>     • Self Attention; • FFN.<br>     • Cross Attention: Only available to decoder.<br>     • Gated Linear Unit (GLU).<br>     • Zero: Return a zero tensor of the input size.<br>     • Identity: Return the input.</td>
    <td class="tg-c3ow">Gradient   optimization (Multi-split reversible network for reducing memory)<br>     &amp; Train a   supermodel </td>
    <td class="tg-c3ow">arxiv 2021-5</td>
  </tr>
  <tr>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
  </tr>
  <tr>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
  </tr>
  <tr>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
  </tr>
  <tr>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">Quantization</td>
    <td class="tg-c3ow">Mixed Precision   Quantization Transformer</td>
    <td class="tg-c3ow">H-level:   1-bit, 2-bit, 4-bit and 8-bit</td>
    <td class="tg-c3ow">Gradient optimization   &amp; Train a supermodel </td>
    <td class="tg-c3ow"> ICASSP 2021</td>
  </tr>
  <tr>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">Other</td>
    <td class="tg-c3ow">TextNAS</td>
    <td class="tg-c3ow">Not Transformer: 1. Convolutional Layers<br>     2.Recurrent Layers 3.Pooling Layers<br>     4.Multi-Head Self-Attention Layers</td>
    <td class="tg-c3ow">RL   same as ENAS &amp; Sample   solutions in a supermodel <br>     (one-shot method)</td>
    <td class="tg-c3ow">AAAI 2020</td>
  </tr>
  <tr>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
  </tr>
  <tr>
    <td class="tg-c3ow">Computer <br>     Vision</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">AutoFormer</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">arxiv 2021-7 (ICCV)</td>
  </tr>
  <tr>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">GLiT</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">arxiv 2021-8</td>
  </tr>
  <tr>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">Multi-stage</td>
    <td class="tg-c3ow">Vit-ResNAS</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">arxiv 2021-9</td>
  </tr>
  <tr>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">PSViT</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">arxiv 2021-8</td>
  </tr>
  <tr>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
  </tr>
  <tr>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
  </tr>
  <tr>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
  </tr>
  <tr>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">Vanilla NAS for CNN</td>
    <td class="tg-c3ow">NAT (not search for   Transformer)</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">PAMI 2021 </td>
  </tr>
  <tr>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
  </tr>
  <tr>
    <td class="tg-c3ow">Speech</td>
    <td class="tg-c3ow">Speech   Recognition</td>
    <td class="tg-c3ow">Evolved   Speech-Transformer</td>
    <td class="tg-c3ow">M-level:   cell space (same as Evolved Transformer) </td>
    <td class="tg-c3ow">EA   &amp; Sample solutions   and  progressive dynamic hurdles (early   stopping)</td>
    <td class="tg-c3ow">INTERSPEECH 2020</td>
  </tr>
  <tr>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">Streaming Transformer</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">arxiv 2020-11</td>
  </tr>
  <tr>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
  </tr>
  <tr>
    <td class="tg-c3ow">Other</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
  </tr>
  <tr>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
  </tr>
  <tr>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
    <td class="tg-c3ow">　</td>
  </tr>
</tbody>
</table>
