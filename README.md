# london-hackday-2016

Things we worked on at the London Lucene Hackday on 7th October 2016.

1. A Browser-driven explorer for Lucene indexes: “Marple”
------------------------------------------------------------
https://github.com/flaxsearch/marple

Luke: https://github.com/DmitryKey/luke

*Alan Woodward leading a team to look at developing this*

2. An absolutely minimal Solr example framework
------------------------------------------------------------
*Erica leading a team to try installing Solr from scratch and note down problems & issues with the examples and guidance*

Erica and Ife gave a great talk on their experience with Solr at a previous Meetup: http://rockthecode.io/tech-events/leveraging-solr-for-website-searches-and-more/

Here's the minimal configuration files they came up with https://github.com/missBerg/solr-resources

Alexandre Rafalovitch has also been working on minimal configs: https://github.com/arafalov/simplest-solr-config and also has a great resource on starting with Solr: http://www.solr-start.com/

3. Different replicas giving different result positions
------------------------------------------------------------
*Christine leading a team to look at the issues with this*

References: https://mail-archives.apache.org/mod_mbox/lucene-solr-user/201301.mbox/%3Czarafa.51006f06.0ea4.1386468330e702d7@mail.openindex.io%3E

  Here is our working branch: https://github.com/fguery/lucene-solr/tree/replicaChoice

  Useful command:
  cd solr/core
  ant test -Dtestcase=DistributedQueryComponentReplicaMarkerTest

4. *Ife looking at Streaming with Solr*
------------------------------------------------------------

5. *Jesse* - SOLR-8396  Add support for PointFields in Solr
------------------------------------------------------------

6. *Diego*: Add BM25F ranking to Lucene https://github.com/diegoceccarelli/solr6-bm25f
------------------------------------------------------------

Other things we didn't get time to look at:

7. Andy Hind's ideas:
I was planning to do some more stuff with min hash. Probably add some support to use it in "more like this". May be look at min hash as part of query/recall expansion during query execution.
Try to get to the bottom of a Japanese Numeric Tokeniser issue that causes intermittent test failures.
Have another go at indexing skip grams for word context stuff......word2vec in SOLR?
Get up to speed with streaming, JDBC and SOLR 6.2.

5. Christine Poerschke: SOLR-6203 & SOLR-8668

6. Christine Poerschke: re-run some static code analysis (Coverity?) of Lucene and/or Solr code e.g. 
https://scan.coverity.com/projects/5620 mentioned on the dev mailing list (http://mail-archives.apache.org/mod_mbox/lucene-dev/201507.mbox/%3cCAFTwexg51-jm_6MDEoz1rEagN3xgkBeTOz5OU_f+mELbOO1POw@mail.gmail.com%3e) in July 2015

7.  Graph searching

---------------------
Thanks to Bloomberg for providing the venue & pizza for lunch and to Alfresco for curry and beers afterwards.

# Boston hackday

This is some of what we worked on during the Boston Lucene hackday on 11th October 2016:

1. Doug Turnbull: BM25F demo with Lucene using BlendedTermQuery and a custom similarity https://github.com/o19s/lucene-bm25f
2. David Smiley: I worked on a new Solr FieldType dedicated to heatmaps.
3. Timothy Rodriguez: working on updating the UnifiedHighlighter to not re-create a token stream for handling automata when doing Analysis.  This should yield reduced memory consumption and hopefully a performance increase for wildcard queries (although likely not much). https://github.com/Timothy055/lucene-solr/commits/master
4. Kevin Watters: A fun day of Solr hacking and coming up with some more examples and use cases for the Solr Graph Query!
5. Steven Bower: Created docker container that builds static/read-only containers with pre-built indexes to allow for hosted/online tutorials
6. Christine Poerschke: created a patch for adding a HelloWorldSolrCloudTestCase class https://issues.apache.org/jira/browse/SOLR-9625, add QParser.getSortSpec https://issues.apache.org/jira/browse/SOLR-9627, cast exception while searching with sort function and result grouping https://issues.apache.org/jira/browse/SOLR-6203
7. Alexandre Rafalovitch: looking at exporting Jira records and generating reports from them that are impossible in Jira itself. Unfortunately, the available export options do not export ALL of the information available (e.g. state transitions), but there is enough to do at least a prototype in a future. Jira also has a more-comprehensive export through XML backup, but I do not have permissions for it. That will need a discussion with INFRA to see if they could do a one-off export to test. We also had a lot of discussion about Solr examples with various people.
8. Keith Laban: Background: When DocValues are enabled on a field that had documents previously indexed values without DocValues it will cause a loss in data. When a DocValuesless segment is merged with a DocValues segment, the new segment will have null DocValues for the DocValueless segment causing missing data in sorting and faceting. Investigated writing a codec to be used when merging to pull the DocValueless document fields from FieldCache and write them as DocValues in the new DocValue segment.
9. Steve Rowe: added some more DocValues functionality to Marple




---------------------
Thanks to BA Insight for providing a venue for the hackday; Flax for providing lunch & Lucidworks for snacks and drinks afterwards.

