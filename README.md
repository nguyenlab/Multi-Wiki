# Multi-Wiki

The corpus is introduced in this paper:

"A Multilingual Parallel Corpus for Improving Machine Translation on Southeast Asian Languages"

in The Machine Translation Summit XVI, Nagoya Japan, 2017.

# multi-wiki

This corpus contains parallel aligned sentences extracted from Wikipedia in languages: Indonesian, Malay, Filipino, Vietnamese, English.


# Building corpora

    1. Extracting parallel titles
    For example: building the English-Indonesian corpus
          
          wget http://dumps.wikimedia.org/enwiki/20170120/enwiki-20170120-page.sql.gz
          wget http://dumps.wikimedia.org/enwiki/20170120/enwiki-20170120-langlinks.sql.gz
          
          wget http://dumps.wikimedia.org/idwiki/20170120/idwiki-20170120-page.sql.gz
          wget http://dumps.wikimedia.org/idwiki/20170120/idwiki-20170120-langlinks.sql.gz
          
          
          ./build-corpus.sh en idwiki-20170120 > en-id-titles.txt
          
    2. Crawl articles using the title pairs
    
    3. Preprocessing: split sentences, word tokenization
    
    4. Sentence alignment 
        
      
        
    5. Truecase, clean
        

# Bilingual Parallel Corpus
Language 1 | Language 2 |  Sentences
------------ | ------------- | -------------
Indonesian | English | 234,380
Indonesian | Filipino | 9,952
Indonesian | Malay | 83,557
Indonesian | Vietnamese | 76,863
Malay | English | 198,087
Malay | Filipino | 4,919
Malay | Vietnamese | 55,613
Filipino | English | 22,758
Filipino | Vietnamese | 10,418
Vietnamese | English | 408,552


# Monolingual Corpus

Language | Sentences
------------ | -------------
Indonesian | 1,478,986
Malay | 596,097
Filipino | 682,939
Vietnamese | 1,862,599



# References

[1] Sentence alignment:
Robert C. Moore (2002): Fast and Accurate Sentence Alignment of Bilingual Corpora, Machine Translation: From Research to Real Users, 5th Conference of the Association for Machine Translation in the Americas, AMTA 2002 Tiburon, CA, USA, October 6-12, 2002, Proceedings

[2] Extracting parallel titles
https://github.com/clab/wikipedia-parallel-titles
