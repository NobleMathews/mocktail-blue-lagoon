# <h1 align="center">**On the Impact of Multiple Source Code Representations on Software Engineering Tasks - An Empirical Study**</h1>
# <h4 align="center">**Mocktail Version - Blue Lagoon**</h4>
<hr/>
<br/>

[Cite this Project](#citation)


* A novel source code representation for capturing syntactic and semantic program features by utilizing multiple intermediate representations of code.

* Previous Versions
  
  * D. Vagavolu, K. C. Swarna and S. Chimalakonda, "A Mocktail of Source Code Representations," *2021 36th IEEE/ACM International Conference on Automated Software Engineering (ASE)*, 2021, pp. 1296-1300, doi: 10.1109/ASE51524.2021.9678551. [[IEEE Xplore]](https://ieeexplore.ieee.org/document/9678551)
  
  * Dheeraj Vagavolu, Karthik Chandra Swarna, and Sridhar Chimalakonda. "On the Impact of Multiple Source Code Representations on Software Engineering Tasks - An Empirical Study" arXiv preprint arXiv:2106.10918 (2021) [[arXiv]](https://arxiv.org/abs/2106.10918)

* Please find the README for both the ```Path Extractor``` tool and the ```Mocktail model``` in their respective folders.

## Datasets
### Method Naming
* Download and create raw datasets using [this](./scripts/clone_repos.py) script.
* Download the processed datasets from [here](https://archive.org/details/mocktail-dataset-method-naming_202302). Processed datasets are path-extracted versions of the raw datasets. They can be readily used to train the model.
* The table below provides a detailed breakdown of this dataset along with the type of project and the number of methods in each:
  
| Repository Name | Project Type | Number of methods |
|---------------------|----------------------------------------------------|-----------------------|
| QMK Firmware | Keyboard firmware | 11,912 |
| FFmpeg       | Multimedia processing libraries | 15,790 |
| OpenSSL | Cryptography and SSL/TLS toolkit | 11,118 |
| Radare2 | Forensic framework & reverse engineering tool | 10,474 |
| ESP-IDF | IoT Development Framework | 13,324 |
| PostgreSQL | Database Management System | 13,190 |
| RT-Thread | Operating system for embedded systems | 82,155 |
| VLC | Multimedia player | 12,091 |
| QEMU | Machine Userspace Emulator | 39,881 |
| GCC | GNU Compiler Collection | 233,689 |
| ZIG | General-purpose programming language | 9,679 |
| KBEngine | Multiplayer game development engine | 21,949 |
| POCO | Libraries to develop network applications | 10,160 |
| SumatraPDF | Multi-format document reader | 16,356 |
| CatBoost | Scalable Gradient Boosting library | 54,365 |
| Fastsocket | Highly scalable socket library | 173,085 |

### Program Classification and Clone Detection
* Download the raw datasets from CodeXGlue's [repository](https://github.com/microsoft/CodeXGLUE/tree/main/Code-Code/Clone-detection-POJ-104#dataset).
* Download the processed datasets from [here](https://archive.org/details/mocktail-dataset-program-classification_202211). Processed datasets are path-extracted versions of the raw datasets. They can be readily used to train the model.

## **Team**
* In case of any queries or if you would like to give any suggestions, please feel free to contact:
  - Karthik Chandra (cs17b026@iittp.ac.in) 
  - Noble Saji Mathews (ch19b023@iittp.ac.in)
  - Dheeraj Vagavolu (cs17b028@iittp.ac.in) 
  - Sridhar Chimalakonda (ch@iittp.ac.in)

 ## Citation

If you use this project in your research, please cite it as follows:

```bibtex
@article{SWARNA2023111941,
title = {On the impact of multiple source code representations on software engineering tasks — An empirical study},
journal = {Journal of Systems and Software},
pages = {111941},
year = {2023},
issn = {0164-1212},
doi = {https://doi.org/10.1016/j.jss.2023.111941},
url = {https://www.sciencedirect.com/science/article/pii/S0164121223003369},
author = {Karthik Chandra Swarna and Noble Saji Mathews and Dheeraj Vagavolu and Sridhar Chimalakonda},
keywords = {Source code representation, Abstract Syntax Tree, Control Flow Graph, Program Dependence Graph, Code embedding, Method naming},
abstract = {Efficiently representing source code is crucial for various software engineering tasks such as code classification and clone detection. Existing approaches primarily use Abstract Syntax Tree (AST), and only a few focus on semantic graphs such as Control Flow Graph (CFG) and Program Dependency Graph (PDG), which contain information about source code that AST does not. Even though some works tried to utilize multiple representations, they do not provide any insights about the costs and benefits of using multiple representations. The primary goal of this paper is to discuss the implications of utilizing multiple code representations, specifically AST, CFG, and PDG. We modify an AST path-based approach to accept multiple representations as input to an attention-based model. We do this to measure the impact of additional representations (such as CFG and PDG) over AST. We evaluate our approach on three tasks: Method Naming, Program Classification, and Clone Detection. Our approach increases the performance on these tasks by 11% (F1), 15.7% (Accuracy), and 9.3% (F1), respectively, over the baseline. In addition to the effect on performance, we discuss timing overheads incurred with multiple representations. We envision this work providing researchers with a lens to evaluate combinations of code representations for various tasks.}
}
```
