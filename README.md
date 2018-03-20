# TASK 2 Topic Extractor
## Overview
This code can be used to extract a topic on a document/article with unsupervised model. This model uses Latent Dirichtlet Allocation (LDA). The workflow of each model is roughly divided in two parts: preprocessing and topic extraction .

## Dependencies
Topic Extractor:
1) Python 3.5
2) pandas 0.22.0
3) nltk 3.2.5
4) regex
5) codecs
6) preprocessor 1.2.3
7) gensim v3.4.0

## Input
to build topic extractor model takes a `.csv` document as input. Each line must consist of article_content columns: 

    Column 1) article_id: unique id of the article
    Column 2) article_topic: main topic of the article
    
## How to run \& output

To run this topic extractor, see the below example.

```
$ python task2LDATopicExtractor.py -h
Options:
  -h, --help           show this help message and exit

   Topic Extractor With LDA :
    Usage: task2LDATopicExtractor.py -f [YOURFILE] -t [NUMBER OF TOPIC]

    -f FILE            Dataset Location(file must be have article_content)
    -t NUM_TOPIC       Number of topics to be extracted

```

So for Topic Extractor With LDA example :

```
$ python task2LDATopicExtractor.py -f ds_asg_data.csv -t 29

Number of Topic = 29
Topic - 0  =  0.065*"darah" + 0.036*"usia" + 0.033*"ganguan" + 0.030*"pembuluh" + 0.026*"penyakit" + 0.023*"gamat" + 0.021*"jely" + 0.014*"obat" + 0.013*"pemesanan" + 0.012*"saluran" 

Topic - 1  =  0.046*"negara" + 0.018*"pasukan" + 0.016*"korea" + 0.016*"presiden" + 0.015*"belanda" + 0.014*"trump" + 0.012*"utara" + 0.010*"militer" + 0.009*"amerika" + 0.008*"dunia" 

Topic - 2  =  0.030*"orang" + 0.015*"senjata" + 0.013*"luka" + 0.011*"korban" + 0.011*"amerika" + 0.011*"serangan" + 0.010*"akibat" + 0.010*"tewas" + 0.008*"kota" + 0.008*"dunia" 

Topic - 3  =  0.024*"gol" + 0.024*"pemain" + 0.019*"laga" + 0.012*"pertandingan" + 0.012*"menit" + 0.012*"bola" + 0.011*"timnas" + 0.010*"berhasil" + 0.010*"tim" + 0.009*"united" 

.
.
.
.
.


Topic - 27  =  0.017*"kondisi" + 0.015*"kulit" + 0.014*"memiliki" + 0.013*"sakit" + 0.013*"mata" + 0.011*"obat" + 0.011*"kesehatan" + 0.009*"dokter" + 0.009*"mengalami" + 0.008*"bayi" 

Topic - 28  =  0.119*"indonesia" + 0.025*"perusahaan" + 0.016*"produk" + 0.014*"online" + 0.011*"jakarta" + 0.011*"kumparan" + 0.008*"kerja" + 0.008*"bisnis" + 0.007*"digital" + 0.007*"layanan" 


Topic Extraction Done ...... 

```
