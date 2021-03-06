# Automatic-Glossary-Terms-Extraction-Using-Word-Embeddings

# Overview 
This repository contains the automatically extracted glossary terms considering two important qualitative attributes, i.e. feature and benefit of the original CrowdRE requirement specifications dataset. In the original CrowdRE dataset, each entry has 6 attributes, i.e., role, feature, benefit, domain, tags and date-time of creation. Since, we are interested in extracting domain-specific terms from this dataset, we only focus on feature and benefit attributes of this dataset. The dataset used in our experiments containing only the feature and benefit attributes of the original CrowdRE dataset can be viewed in the file named "CrowdRE Requirements Dataset.csv". However, the original CrowdRE dataset is devloped by P. K. Murukannaiah et al. and can be accessed from "The smarthome crowd requirements dataset", https://crowdre.github.io/murukannaiah-smarthome-requirements-dataset/, April, 2017. 

# Approach
Along with the glossary set, we have also computed and reported the ground truth set for a random subset of 100 requirement specifications of the used CrowdRE dataset. In total, we have extracted a total of 304 glossary terms and 250 ground truth terms. The ground truth terms have been calculated from our intuition and also utilizing some existing ground truth set ("T. Gemkow, M. Conzelmann, K. Hartig and A. Vogelsang, Automatic Glossary Term Extraction from Large-Scale Requirements Specifications, IEEE 26th International Requirements Engineering Conference (RE), 2018, pp. 412-417.") in an unbiased manner, as there exists no benchmark or gold standard related to the ground truth, whereas the glossary terms are extracted and included in the final set based on the computed similarity scores using the word embedding based word2vec model. The file "Glossary and Ground Truth Set.csv" highlights the extracted glossary terms (a total of 304) and ground truth terms (a total of 250).   

For finding similar noun phrases and computing their similarity scores, we have used a similar topic related dataset, i.e. Wikipedia Home Automation Category, "https://en.wikipedia.org/wiki/Category:Home_automation" and extracted the web pages for a depth of two considering the tree structure wikipedia category. The main reason for selecting and using the data of "Wikipedia Home Automation" in our experiments, because it is very much related and more relevant to the topic of smart home. 

# Evaluation
The file "Glossary Similarity Scores.pdf" reports the calculated cosine similarity scores in alphabetical order for the extracted glossary terms (noun phrases) that are included in the final glossary set using our approach. The similarity scores are computed for the same noun phrases that are common to both the used datasets, i.e. CrowdRE dataset and Wikipedia Home Automation Category dataset. In the final glossary set, we have included all those noun phrases which are having a semantic similarity (cosine similarity) score greater than or equal to 0.5. The range of the similarity score is between 0 to 1. The scores closer to 1 means that the words are semantically more similar. On the other hand, scores closer to 0 means that the words are less related to each other. On these basis, we have selected and included all the noun phrases in the final glossary set only considering the values of similarity score, which acts as a filter in our used approach.

# Publication Details

If you find the above mentioned details useful for your research, please cite the following paper.

Siba Mishra, Arpit Sharma. Automatic Word Embeddings-Based Glossary Term Extraction from Large-Sized Software Requirements. In Proceedings of the 25th International Working Conference on Requirements Engineering: Foundation for Software Quality (REFSQ), 2020, Pisa, Italy. pp. 203-218. DOI: https://doi.org/10.1007/978-3-030-44429-7_15


