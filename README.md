# Facts chain extractor
This project contains:
1. Examples of the use of https://github.com/IINemo/isanlp and https://github.com/IINemo/isanlp_srl_framebank
2. Code for extracting tuples (predicate, arguments). Code in development. There is a bug in the group extraction function. We will add a generalization of arguments using word embeddings.

# Installation
Note: the library is considered for Python 3.6.
1. Install IsaNLP and its dependencies:
```
pip install grpcio
pip install git+https://github.com/IINemo/isanlp
```  
2. Install IsaNLP SRL FrameBank library:
```
pip install git+https://github.com/IINemo/isanlp_srl_framebank
```  
3. Deploy docker containers for morphology, syntax, and SRL parsing:  
```
docker run -d --rm -p 3333:3333 inemo/isanlp
docker run -d --rm --shm-size=1024m -ti -p 3334:9999 inemo/syntaxnet_rus server 0.0.0.0 9999
docker run -d --rm -p 3335:3333 inemo/isanlp_srl_framebank
```  
