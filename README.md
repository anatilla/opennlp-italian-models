opennlp-italian-models
======================

PROJECT SCOPE
This project collects documentation and models for natural language processing with the Apache OpenNLP Toolkit in Italian language.

The models created are:
  - Maxent POS Tagger
  - Perceptron POSTtagger 
  - Sentence Detector
  - Tokenizer

For documentation and explanation of the role and use of each model, please see [1].

CORPORA AND TRAINING SETS
As training sets for POSTagger and Tokenizer models we have used a big annotated corpus, taken from the italian version of Wikipedia and annotated with a semi-automatic process.
The corpus has been made available with an open source license by the University of Bologna (thanks to them for sharing it); see [2] for a reference to the page, where the corpus is shared.
To train the Sentence Detector Models we have used a documents with 1500 sentences annotated manually, taken from italian Wikipedia, too.
All the models have been trained with the OpenNLP training tools available in version 1.5.3.

TAGSET
To train the POSTagger models we have defined a tag dictionary, fitted for the italian language, that is a subset of the Tanl tag dictionary, a standard tagset implementation, compliant with the EAGLES international standards. See [3] for a definition of the original Tanl tagset.
The customized version of the tag dictionary, used for annotating the corpora, and that the POS Tagger will produce on italian sentences, is available inside the project, (openNLP-it/lang/it/pos/tagsDictionaryIt.txt).

ACCURACY
To test the accuracy of the POS Tagger and Tokenizer models we have used a "uniform" test corpora, taken from the italian version of Wikipedia (but completely disjointed from the training corpora).
OpenNLP evaluator extimated we achieved the following results:
  - POS Maxent and Perceptron accuracy: 97.56%
  - Tokenizer Precision: 99%

The complete evaluation reports are avalilable inside the project under the following folders: 
openNLP-it/lang/it/pos/data/pos-maxent
openNLP-it/lang/it/pos/data/pos-perceptron
openNLP-it/lang/it/token/data

REFERENCES
[1] OpenNLP developer documentation Version 1.5.3,
http://opennlp.apache.org/documentation/1.5.3/manual/opennlp.html

[2] Corpora shared with different licenses from the University of Bologna,
http://wacky.sslmit.unibo.it/doku.php?id=corpora#italian
http://wacky.sslmit.unibo.it/doku.php?id=download

[3] Tanl tagset definition (fitted for italian language),
http://medialab.di.unipi.it/wiki/Tanl_POS_Tagset
