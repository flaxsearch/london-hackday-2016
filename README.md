# london-hackday-2016
Work for the Lucene/Solr London meetup hackday, 7/10/2016

Ideas for the Hackday:

1. A Browser-driven explorer for Lucene indexes: “Marple”
https://github.com/flaxsearch/marple
Luke: https://github.com/DmitryKey/luke
*Alan Woodward leading a team to look at developing this*

2. Andy's ideas:
I was planning to do some more stuff with min hash. Probably add some support to use it in "more like this". May be look at min hash as part of query/recall expansion during query execution.
Try to get to the bottom of a Japanese Numeric Tokeniser issue that causes intermittent test failures.
Have another go at indexing skip grams for word context stuff......word2vec in SOLR?
Get up to speed with streaming, JDBC and SOLR 6.2.

3. An absolutely minimal Solr example framework
*Erica leading a team to try installing Solr from scratch and note down problems & issues with the examples and guidance*

4. Different replicas giving different result positions
*Christine leading a team to look at the issues with this*
References: https://mail-archives.apache.org/mod_mbox/lucene-solr-user/201301.mbox/%3Czarafa.51006f06.0ea4.1386468330e702d7@mail.openindex.io%3E

5. Christine: SOLR-6203 & SOLR-8668

6. Christine: LUCENE-6911

7.  Graph searching

8. *Ife looking at Streaming with Solr*

9. Diego: BM25F
