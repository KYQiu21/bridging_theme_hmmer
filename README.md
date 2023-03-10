# HMMER Bridging Theme Dataset

This is the bridging theme dataset and releated scripts of this paper: [Similar protein segments shared between domains of different evolutionary lineages. Qiu, K., Ben‐Tal, N., & Kolodny, R. (2022). Protein Science, 31(9), e4407.](https://onlinelibrary.wiley.com/doi/10.1002/pro.4407) For any questions, please contact <kaiyuqiu4@gmail.com> for help.

## Description

The dataset is organized in Cytoscape and our pluggin [CyToStruct](https://www.sciencedirect.com/science/article/pii/S0969212615000763) for launching external apps (such as PyMOL and BioEdit) for nodes/edges. Below are one-to-one explanations about files in this repo.


**yaml_cross_fold_themes_with_domains**: YAML script for the configuration of Cytoscape/CyToStruct networks.

**optAlign.py**: Python script for structure alignment.

**overview.cys**: Overview Cytoscape network file of all bridging themes (Fig. 1 of the paper).

**hmmer_bridging_themes.cys**: Cytoscape network file with each X-group pair separated. 

**domain_cs_node_props**: Table of attributes of nodes in *overview.cys* (ECOD domain, ECOD F-group ID, ECOD X-group ID, ECOD X-group name).

**overview_pvalue_10-3(_minlen)**: Table of X-group ID pairs (with a lenghth 20 residues as the minimum limitation).

**cy2str_edge_data(_pval_10-3)**: Table of detected bridging theme, including egde name, ECOD domain 1, ECOD domain 2, residue range 1, residue range 2, sequence similarity and identity (with 1e-3 as the threshold of P-value). 

**cy2str_asdb.zip**: Directory containing sequence alignments of each bridging theme pair.

**pdbs.zip**: Directory containing all ECOD PDB files involved in this dataset.


## Usage

To play with this dataset, CyToStruct application should be installed in Cytoscape at first. 

To look into a specific bridging theme pair in the network, you should:
1. Configure Cytoscape with the YAML script *yaml_cross_fold_themes_with_domains* (Apps -> Configure CyToStruct -> load file, please revise the YAML script according to this [tutorial](https://bitbucket.org/sergeyn/cytostruct/wiki/Home)).
2. For a specific bridging theme (an edge in the network), right-click the edge and go to PyMOL/BioEdit to see the structure and sequence alignment.  






