# OSR_RoR_SemEval
Ontology-style relation annotation datasets: Japanese traffic rules of the road and SemEval-2010 Task 8

## Description of this data

Each dataset is in two different formats: (1) Conventional annotation (Normal-RoR stands for the Japanese traffic Rules of the Road) and (2) Ontology-Style Relation (OSR) annotation (OSR-RoR stands for Normal-RoR in OSR format, and OSR-SemEval stands for SemEval-2010 Task 8 in OSR format). 
* Normal-RoR: Japanese traffic Rules of the Road dataset that are in conventional annotating format using direct links to maintain relationships between entities.
  * Normal-RoR_all.json: Contain the whole dataset.
  * Folders (1, 2, 3, 4, 5): Contain the five-crossed validating data created from the Normal-RoR.json:
    * train.json: Training dataset
    * dev.json: Validating dataset
    * test.json: Testing dataset
* OSR-RoR: Japanese traffic Rules of the Road dataset that are in Ontology-Style Relation (OSR) annotating format using relation mentions and some RDF standard properties to maintain relationships between entities.
  * OSR-RoR_all.json: Contain the whole dataset.
  * Folders (1, 2, 3, 4, 5): Contain the five-crossed validating data created from the OSR-RoR.json:
    * train.json: Training dataset
    * dev.json: Validating dataset
    * test.json: Testing dataset
    
* OSR-SemEval.json: SemEval-2010 Task 8 dataset that are in Ontology-Style Relation (OSR) annotating format using relation mentions and some RDF standard properties to maintain relationships between entities.

The differences between the conventional annotation and the OSR are: (1) In the conventional annotation, a direct link is used to maintain relationship between two entities, and (2) In OSR, a relation mention, which is a word or phrase that can represent relationships, is used to maintain relationship between two entities by using “domain” and “range” connecting from the relation mention to the two entity mentions. 

## Steps to reproduce
Both datasets are publicly available and can be freely downloaded from the Internet (Ref: [2], [3]). They are in plain text, which were manually annotated by human annotators by selecting all entities and labeling their relationships. The RoR dataset [2] is in Japanese, but the annotation of all entities and relations is in English. The SemEval dataset [3] is in English. The annotations of both data are done by using BRAT [4], which is a Web-based tool for NLP-assisted text annotation.

The Japanese traffic Rules of the Road is in pure text. When creating Normal-RoR and OSR-RoR, all key words/phrases (entities) that are related to traffic rules are chosen. The relationships between entities are annotated so that the original meanings are maintained as much as possible. 
In the OSR-SemEval dataset, all entities are given, the criteria to maintain the relationships of all entities is to find words/phrases in the sentences that can represent the relationships. 
It is important to emphasize that both datasets were annotated by the humans.

## References
* [1] Savong Bou, Naoki Suzuki, Makoto Miwa, Yutaka Sasaki, “Ontology-style relation annotation: A case study”, in: Proceedings of the 12th Language Resources and Evaluation Conference, European Language Resources Association, Marseille, France, 2020, pp. 4867–4876. URL https://aclanthology.org/2020.lrec-1.599
* [2] National Public Safety Commission, Notice No. 3, Instructions on transportation methods, Japan, 1978, https://www.npa.go.jp/koutsuu/kikaku/kyousoku/index.htm.
* [3] Iris Hendrickx, Su Nam Kim, Zornitsa Kozareva, Preslav Nakov, Diarmuid Ó Séaghdha, Sebastian Padó, Marco Pennacchiotti, Lorenza Romano, Stan Szpakowicz, “SemEval-2010 Task 8: Multi-Way Classification of Semantic Relations between Pairs of Nominals,” in: Proceedings of the 5th International Workshop on Semantic Evaluation, July, 2010, Uppsala, Sweden, pp. 33-38. URL https://www.kaggle.com/datasets/drtoshi/semeval2010-task-8-dataset  
* [4] Pontus Stenetorp, Sampo Pyysalo, Goran Topic, Tomoko Ohta, Sophia Ananiadou, Jun'ichi Tsujii, “brat: a web-based tool for nlp-assisted text annotation,” in: EACL 2012, 13th Conference of the European Chapter of the Association for Computational Linguistics, Avignon, France, April 23-27, 2012, 2012, pp. 102–107. URL https://www.aclweb.org/anthology/E12-2021/

## Related links
* https://www.npa.go.jp/koutsuu/kikaku/kyousoku/index.htm
  * Article is derived from this dataset
* https://www.kaggle.com/datasets/drtoshi/semeval2010-task-8-dataset
  * Dataset is derived from this dataset
* https://aclanthology.org/E12-2021/
  * Software compiles this dataset
* https://aclanthology.org/2020.lrec-1.599/
  * Article is related to this dataset
* https://aclanthology.org/S10-1006/
  * Article is source of this dataset
