# london-hackday-2016
Work for the Lucene/Solr London meetup hackday, 7/10/2016

Ideas for the Hackday:

---things we're working on---

1. A Browser-driven explorer for Lucene indexes: “Marple”
https://github.com/flaxsearch/marple
Luke: https://github.com/DmitryKey/luke
*Alan Woodward leading a team to look at developing this*

3. An absolutely minimal Solr example framework
*Erica leading a team to try installing Solr from scratch and note down problems & issues with the examples and guidance*
Erica and Ife gave a great talk on their experience with Solr at a previous Meetup: http://rockthecode.io/tech-events/leveraging-solr-for-website-searches-and-more/

4. Different replicas giving different result positions
*Christine leading a team to look at the issues with this*
References: https://mail-archives.apache.org/mod_mbox/lucene-solr-user/201301.mbox/%3Czarafa.51006f06.0ea4.1386468330e702d7@mail.openindex.io%3E

Here is our working branch: https://github.com/fguery/lucene-solr/tree/replicaChoice

Useful command:
cd solr/core
ant test -Dtestcase=DistributedQueryComponentReplicaMarkerTest

8. *Ife looking at Streaming with Solr*

10. SOLR-8396  Add support for PointFields in Solr

---parked for now---

2. Andy's ideas:
I was planning to do some more stuff with min hash. Probably add some support to use it in "more like this". May be look at min hash as part of query/recall expansion during query execution.
Try to get to the bottom of a Japanese Numeric Tokeniser issue that causes intermittent test failures.
Have another go at indexing skip grams for word context stuff......word2vec in SOLR?
Get up to speed with streaming, JDBC and SOLR 6.2.

5. Christine: SOLR-6203 & SOLR-8668

6. Christine: re-run some static code analysis (Coverity?) of lucene and/or solr code e.g. 
https://scan.coverity.com/projects/5620 mentioned on the dev mailing list (http://mail-archives.apache.org/mod_mbox/lucene-dev/201507.mbox/%3cCAFTwexg51-jm_6MDEoz1rEagN3xgkBeTOz5OU_f+mELbOO1POw@mail.gmail.com%3e) in July 2015

7.  Graph searching

9. Diego: BM25F
