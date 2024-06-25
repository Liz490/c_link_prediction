# linkpred

This project in the context of the lecture "Machine Learning for Regulatory Genomics" at TU Munich tries to improve the understanding of regulatory mechanisms in cells involving long non-coding RNAs (lncRNA). We investigate how lncRNA, messenger RNA (mRNA), and other molecules interact
with each other, what functions they serve, what roles they play in gene regulation, and other cellular
processes. In order to do so, we perform link prediction in biomedical knowledge graphs. We use a pathbased
reasoning graph neural network (GNN) building on NBFnet [29] and evaluate it against other stateof-
the-art knowledge graph embedding methods, such as TransE and RotatE. The resulting predictions
could potentially be used to explain aspects of known regulatory mechanisms, explore unknown ones, and
design novel experiments.

For more details see the report contained in the repository. (/C_Link_Prediction_in_Biological_Knowledge_Graphs.pdf)

## GIT Submodule
To run the nbfnet, you need to load a GIT submodule via the following commands: 
```
git submodule init; git submodule update 
```
To update the submodule use
```
git submodule update --remote --rebase
```
## NBFNet container

Use the following commands to build and run NBFNet in a docker container.

```bash
docker build -f docker/nbfnet/Dockerfile . -t nbfnet:latest
docker run -ti --rm --gpus all nbfnet:latest bash
```
