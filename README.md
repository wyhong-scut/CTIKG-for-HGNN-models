# CTIKG-for-HGNN-models

The construction of a knowledge graph automatically has been the subject of much recent CSKG research, however few of these studies have chosen to make their knowledge base publicly available, which has hampered the advancement of downstream applications like knowledge representation learning on CSKG. 

The application of CSKG encounters two major challenges:

1. Reproducing earlier research on knowledge graph construction is necessary and may incur costs.

2. Different CSKGs have different ontologies and data sources, therefore researchers need to consider if the existing CSKGs could be applied to their work.

Eleven node types are included in CTIKG and are created in accordance with STIX 2.0. Infrastructure ontology only depicts the attacker side without objective information. Specific node types and links from the src node type to the dst node type are listed in Table 1 and Table 2. The statistics of CTIKG are shown in Table 3.

**Table 1 Specific node types in CTIKG**

| ID  |    Node Type     |
|:---:|:----------------:|
|  0  |  attack_pattern  |
|  1  |     campaign     |
|  2  | course_of_action |
|  3  |    indicator     |
|  4  |  infrastructure  |
|  5  |     malware      |
|  6  |  observed_data   |
|  7  |      report      |
|  8  |   threat_actor   |
|  9  |       tool       |
| 10  |  vulnerability   |

**Table 2 Links from src node type to dst node type in CTIKG**

| ID  | SRC Node Type ID -> DST Node Type ID |
|:---:|:------------------------------------:|
|  0  |              0 -> 10                 |
|  1  |              2 -> 0                  |
|  2  |              2 -> 10                 |
|  3  |              3 -> 1                  |
|  4  |              3 -> 4                  |
|  5  |              3 -> 5                  |
|  6  |              4 -> 6                  |
|  7  |              5 -> 9                  |
|  8  |              6 -> 7                  |
|  9  |              7 -> 3                  |
| 10  |              7 -> 8                  |
| 11  |              7 -> 10                 |
| 12  |              7 -> 1                  |
| 13  |              8 -> 0                  |
| 14  |              8 -> 4                  |
| 15  |              8 -> 9                  |
| 16  |              9 -> 5                  |

**Table 3 Statistics of CTIKG**

| Dataset | #Nodes | #Node Types | #Edges |
|:-------:|:------:|:-----------:|:------:|
|  CTIKG  | 13586  |     11      | 16869  |

CTIKG is intrinsic a heterogeneous graph, so we preprocessed the dataset in the format of [HGB](https://www.biendata.xyz/hgb). Experiment results on HGB will be updated later.
