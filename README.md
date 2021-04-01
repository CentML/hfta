# hfta

<img src="docs/intro.gif" alt="Horizontally Fused Training Array" width="700">

--------------------------------------------------------------------------------

_**H**orizontally **F**used **T**raining **A**rray_ (HFTA) is a [PyTorch](https://pytorch.org/) extension 
library that helps machine learning and deep learning researchers and practitioners to develop horizontally 
fused models. Each fused model is functionally/mathematically equivalent to an array of models with 
similar/same operators. 

Why developing horizontally fused models at all, you ask? This is because sometimes training a certain 
class of models can _under-utilize_ the underlying accelerators. Such hardware under-utilization could then 
be _greatly amplified_ if you train this class of models _repetitively_ (e.g., when you tune its 
hyper-parameters). Fortunately, in such use cases, the models under repetitive training often have the 
_same types_ of operators with the _same shapes_ (e.g., think about what happens to the operators when 
you adjust the learning rate). Therefore, with HFTA, you can improve the hardware utilization by training 
an array of models (as a single fused model) on the same accelerator at the same time.

## Installation

### From Source

```
git clone https://github.com/UofT-EcoSystem/hfta.git hfta/
pip install -e hfta/
```

### From PyPI

TODO

## Getting Started

TODO

## Publication

- Fourth Conference on Machine Learning and Systems ([MLSys'21](https://mlsys.org/))
  - [Horizontally Fused Training Array: An Effective Hardware Utilization Squeezer for Training Novel Deep Learning Models](https://mlsys.org/virtual/2021/oral/1610)
    - [Proceedings](https://proceedings.mlsys.org/paper/2021/hash/a97da629b098b75c294dffdc3e463904-Abstract.html)
    - [Talk](https://youtu.be/zJ5UUb0J9tI)
    - [arXiv](https://arxiv.org/abs/2102.02344)
    - Please refer to the [MLSys'21 Artifact Reproduction Guide](docs/mlsys21/README.md) on how to reproduce the reported experiments.

## Contributing

We sincerely appreciate contributions! We are currently working on the contributor guidelines. For now, just send us a PR for review!

## License

HFTA itself has a [MIT License](LICENSE). When collecting the [examples](examples/) and [benchmarks](benchmarks/), we leverage other
open-sourced projects, and we include their licenses in their corresponding directories.

## Authors

HFTA is developed and maintained by Shang Wang ([@wangshangsam](https://github.com/wangshangsam)), 
Peiming Yang ([@ypm1999](https://github.com/ypm1999)), Yuxuan Zheng ([@eric-zheng](https://github.com/eric-zheng)), 
Xin Li ([@nixli](https://github.com/nixli)). HFTA is one of the research projects from the 
[EcoSystem](https://www.cs.toronto.edu/ecosystem/) group at the [University of Toronto](https://www.utoronto.ca/), 
[Department of Computer Science](https://web.cs.toronto.edu/).
