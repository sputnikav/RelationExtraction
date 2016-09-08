#### RelationExtraction
<<<<<<< HEAD
Tasks: 
-Acquire useful information from unstructured text. 
-Build knowledge graph based on extracted information 
-Domain: banking – finance.

### 1. Aspect linking

The approach is divided into 3 steps:
+ extract term-aspect pairs (using CRF suite)
+ build a path to link term-aspect (using Dependency tree)
+ update the dictionary “bank-aspect”

In this experiment, we focus on extracting brand-aspect relations (brands set includes ACB, Agribank, BIDV, Eximbank, Maritime, Sacombank) and neglect the aspect related to sub-fields, such as “Bankplus” – “dịch vụ”. According to the nature of Dependency parsing, we can exploit Dependency tree either as directed/undirected graph for this task. 

Along with extracting information from queried data, we also try to enhance the quality of Dependency parser (moving to Universal dependency) and POS tagger. New training data for these two models are released.
We also attempt to evaluate the performance of Dependency Parsing based on UAS and LAS (for each label).

### 2. Using templates (triples):
Extract the relations that belong to one of these three following templates:
Template 1: [nsubj – verb – dobj]
Template 2: [nsubj – verb – prep – pobj]
Template 3: [nsubj – verb – dobj – prep – pobj]
In this task, we strictly employ Dependency tree as directed graph.
In this task, we consider only Noun phrases for finding Nsubj, dobj, pobj.

### 3. Bootstrapping method

The method is based on two sources:
+ A small number of initial instances (in our case, the relation between organization and employee)
+ A large number of unannotated text.


=======
Tasks: -Acquire useful information from unstructured text. -Build knowledge graph based on extracted information -Domain: banking – finance.
>>>>>>> master
