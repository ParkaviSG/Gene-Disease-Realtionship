### Gene-Disease-Realtionship
The preprocessing of a pubmed central full text document (PMCID: PMC2837563)
which includes the tagging of gene and disease entities using the PubTator Central API, followed by the splitting of the segments into sentences, masking of gene and disease terms in those sentences with @Gene$ and @Disease$ respectively. 
There is a unique index assigned to each sentence and the preprocessed and original sentences are stored in separate files with their respective indices. 
Original sentences are stored under: ‘BioBert/biobert-pytorch/relation-extraction/pubtator_outputs’
Processed sentences are stored under: ‘BioBert/biobert-pytorch/relation-extraction/testset’ for BioBert testing purposes.
The BioBert model is now fine tuned on the publicly available GAD - Gene Disease Association Dataset for the relationship extraction task. 
The fine tuned BioBert model is now applied to make predictions for the preprocessed sentences of the given pubmed central document. It provides an output 1 if the entities are related to each other else 0. 
The outputs are stored into ‘BioBert/biobert-pytorch/relation-extraction/pubtator_outputs/final_relation_extraction_output.csv’
