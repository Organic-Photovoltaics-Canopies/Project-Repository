# AI-Powered Design of Organic Photovoltaics

![Senior Design Final Poster](./Poster.pdf)

## [Patent Fetching](./patent-fetch-pipline/)

## [Variational Graph Autoencoder](./vgae/)

###### [Augmented Graph Notebook](./vgae/src/augmented-graphs.ipynb)
- Input is the [OPV2D Dataset](https://github.com/sunyrain/OPV2D/blob/main/Active_Database.csv)
- Converts SMILES to RDKit molecules, then PyG graphs
- Adds chemBERTa embeddings as a graph feature
- Exports `graphs_cached.pt` which consists of:
    - 'df' - a modified version of the OPV2D DataFrame which includes the new graph objects
    - 'atom_vocab' - a dictionary mapping atom ids to the corresponding atomic numbers
    - 'bond_vocab' - a dictionary mapping bond ids to the corresponding bond type (RDKit Object)
    - 'max_mol_size' - The number of atoms in the largest molecule of the dataset

###### [VGAE](./vgae/src/vgae.ipynb)
- Based on [A Two-Step Graph Convolutional Decoder for Molecule Generation](https://doi.org/10.48550/arXiv.1906.03412) by Bresson and Laurent
- Current implementation is too VRAM intensive, needs optimization

## [Graph Diffusion](./graph-diffusion/)
