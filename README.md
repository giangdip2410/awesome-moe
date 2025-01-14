# awesome-moe

With the MoE applying in Transformers to enlarge the parameter size while not enlarging the training and inference costs, MoE has been popular for giant model. In this repo, multiple design will be linked to corresponding papers and projects, to provide a aggregation of MoE studies.
## Diverse MoE Design
[Sparse Gate with topK, 2017](https://openreview.net/pdf?id=B1ckMDqlg): which is the most widely applied MoE architecture, using the gating function to sparsely activate each expert models (with topK values) to be trained and using expert models' merging decision as the inference. 
[Code1](https://github.com/davidmrau/mixture-of-experts)
[Code2](https://github.com/jsuarez5341/Efficient-Dynamic-Batching)
[Code3](https://github.com/ma921/XRDidentifier) 
<div align=center>
<img src="https://github.com/giangdip2410/awesome-moe/raw/main/pictures/sparse%20gate.png" height="300" />
</div>  

  [Expert Gate, 2017](https://openaccess.thecvf.com/content_cvpr_2017/papers/Aljundi_Expert_Gate_Lifelong_CVPR_2017_paper.pdf): binding each expert with a autoencoder, making sure every data can be consistently sent to corresponding expert model.  
<div align=center>
<img src="https://github.com/giangdip2410/awesome-moe/raw/main/pictures/expert%20gate.png" height="300" div align=center/>  
</div>  

  [Multi-gate, 2018](https://dl.acm.org/doi/pdf/10.1145/3219819.3220007): applied multiple gates for multiple unrelated tasks to help better training and inference.  
<div align=center>
<img src="https://github.com/giangdip2410/awesome-moe/raw/main/pictures/multi%20gate.png" height="300" div align=center/>  
</div>  

  [DenseToSparse, 2021](https://arxiv.org/pdf/2112.14397.pdf): training the MoE network first using all experts, raising the hurdle after epoch and epoch, and finally resulting in one-hot or topK experts, which balance the FLOPs and achieve better model quality. 
<div align=center>
<img src="https://github.com/giangdip2410/awesome-moe/raw/main/pictures/dense2sparse.png" height="300" div align=center/>  
</div>  

## Transformer with MoE
  [Switch Transformer, 2021](https://arxiv.org/pdf/2101.03961.pdf): using the sparse gate MoE to route the token to a specific FFN expert.  
<div align=center>
<img src="https://github.com/giangdip2410/awesome-moe/raw/main/pictures/Switch%20Transformer.png" height="300" div align=center/>  
</div>  

  [VLMo, 2021](https://arxiv.org/pdf/2111.02358.pdf): using MoE as a multi-modal FFN controller(for text, image and image_text).  
<div align=center>
<img src="https://github.com/giangdip2410/awesome-moe/raw/main/pictures/vlmo.png" height="300" div align=center/>  
</div>  

## MoE System
[fastmoe](https://github.com/laekov/fastmoe)([paper](https://arxiv.org/pdf/2103.13262.pdf)): A easy-to-hand-on system for MoE developer, optimizing the system scheduling.  
[tutel](https://github.com/microsoft/tutel): optimization on communication.  
