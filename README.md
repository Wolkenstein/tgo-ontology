
# Text Graph Ontology

This ontology is aimed at representing a text variation graph.

For documentation see https://wolkenstein.github.io/tgo-ontology/.

Ontology versions:
- tgo_current.owl: current version, using namespace http://www.hinkelmanns.at/tgo/.
- tgo_0-1.owl: Versioned ontologie, using namespace http://www.hinkelmanns.at/tgo/0.1/.

## Description

### Abstract 

*A model of text as a variant graph can support representing genetic text editions. The proposed model makes it possible to describe the relations between tokens and their relative dependencies in text genesis. The main focus is on the representation of intradocumentary text revisions. Moreover the Text-Graph-Ontology enables the referencing of genetic text editions via the Semantic Web.*

### Introduchtion

Text genetic editions are enjoying sustained popularity in the fields of scholarly editions and literary studies. Representatives of recent research projects are the Faust edition (Bohnenkamp, Henke, and Jannidis 2016) or the edition of the works of Arthur Schnitzler (Burch et al. 2016), both of which aim at a complete reproduction of the text genesis. These editions require the reconstruction of complex text genetic processes. Which sequence of tokens forms a specific text state? How can differences between versions be described? The extension of the model of the Text Encoding Initiative by elements required for genetic editions was the subject of a working group that presented its results in a draft (Burnard et al. 2010). Parts of this draft have been incorporated into the TEI Guidelines (TEI Consortium 2013). With TEI P5, complex genetic editions can be realized. However, the underlying structure of the hierarchical graph makes it difficult to reconstruct and compare text gradients, i.e. the evolutionary stages of a text with inline markup. It can of course be done using stand-off and out-of-line annotations, as James Cummings has pointed out (Cummings 2018, 13). This concept for a Text Graph Ontology does not aim to be the next paper criticizing the xml foundation of TEI P5 nor is it trying to compete with the interoperability of TEI encoded texts. The ontology is designed for the specific purpose of implementing a text variant graph using semantic web technologies for the encoding of genetic text editions.

### Data models for textual representation

Several project used graphs to represent textual variation in the recent years. They can be divided into methods based on markup and methods focusing on variant graphs. An approach to deal with the problem of overlapping annotations in XML is the proposed markup language ‘General Ordered-Descendant Directed Acyclic Graph’ (GODDAG: Sperberg-McQueen and Huitfeldt 2004, esp. 158). A similar model is the ‘Graph Annotation Format’ (GrAF: Ide and Suderman 2007) which extends the Linguistic Annotation Framework (LAF: Ide and Romary 2006). In GRaF an underlying text is segmented via stand-off nodes, which use the position of characters in the text as reference points. Edges link the annotations with text segments. 

The problem of intradocumentary and intertextual variation is addressed by the ‘data structure for representing multi-version texts’ (Schmidt and Colomb 2009). Thy criticize the markup approach of models like GODDAG and GrAF (Schmidt and Colomb 2009, 499) and propose a variant graph where the edges contain the segments of texts shared by multiple variants.

Collating texts is the focus of the stemmaweb project (“The Stemmaweb Project” 2012–; Andrews and Mace 2013). Similar to Schmidt and Colomb 2009 a variation graph is used to represent versions of a text. The texts are segmented into tokens and form the nodes of the graph. Directed edges show the similarities and dissimilarities between individual text carriers. Undirected edges represent variant relationships like orthographic variation, grammatical variation, lexical variation etc. (Andrews and Mace 2013, 508).

Efer 2016 has comprehensively described the use of graph databases for the text-oriented Digital Humanities. He proposed ‘Kadmos’, a layered graph model for textual representation. His model includes the separation into types and tokens. The ‘Text as Graph’ model (TAG: Haentjens Dekker and Birnbaum 2017) stores the text in nodes of various length (Haentjens Dekker and Birnbaum 2017, §3).

This very brief overview of selected data models for textual representation has shown, that multiple models for the representation of texts as graphs exist. The proposed model of this paper is far from state of a stable model and aims to connect the idea of a variation graph with semantic web technologies.

### Text Graph Ontology

The Semantic Web makes information accessible in a machine-readable way using standardized vocabularies and ontologies.  A distinction is made between ‘nodes’, which can be objects or atomic values, and ‘edges’, which describe the relationship between nodes. A statement always consists of a triple ‘[subject] - [predicate] - [object]’. Semantic Web technologies enable easy annotating and linking the scholarly genetic edition other resources. The Text Graph Ontology uses the Web Ontology Language (OWL: W3C OWL Working Group 2012) to specify classes and properties.

![Basic](diagrams/tgo-diagrams-Basic%20RDF.png)

The first problem which needs to be addressed is the segmentation of a text. There is no agreement between the briefly presented models on what the atomic unit of a text graph is. For the Text Graph Ontology tokens separated by white space should be assumed, with the possibility to extend the model on a sub token level. A diplomatic transcription and various normalization stages can be attached to a token as a string or generatet from a separated character graph.

The proposals for the annotation of text revisions of the Grazer Editionsphilogie are tailored to the needs of mediaeval editions. Hofmeister-Winter 2016 presents a categorization of text revision phenomena. She distinguishes between self-revisions, i.e. interventions in one's own text, and external revisions, which describe the interventions of another hand (Hofmeister-Winter 2016, 10). Self-revisions can be a direct component of text production (immediate revision) or take place at a later point in time (late revision). In their opinion, third-party revisions, on the other hand, take place exclusively in a later revision step as a late revision.

TGO uses an edge weighted directed acyclic graph to represent text. To enable the use of weight in a RDF-enviroment, the weighted edges are realised as nodes.

#### Basics



### References

Andrews, T. L., and C. Mace. 2013. “Beyond the Tree of Texts: Building an Empirical Model of Scribal Variation Through Graph Analysis of Texts and Stemmata.” _International Journal of Human-Computer Studies_ 28 (4): 504–21. doi:10.1093/llc/fqt032.

Bohnenkamp, Anne, Silke Henke, and Fotis Jannidis. 2016. “Johann Wolfgang Goethe: Faust: Historisch-Kritische Edition.” 2. Beta-Version. Accessed April 26, 2017. http://beta.faustedition.net/.

Burch, Thomas, Stefan Büdenbender, Kristina Fink, Vivien Friedrich, Patrick Heck, Wolfgang Lukas, Kathrin Nühlen et al. 2016. “Text[ge]schichten: Herausforderungen Textgenetischen Edierens Bei Arthur Schnitzler.” In _Textgenese Und Digitales Edieren: Wolfgang Koeppens „Jugend“ Im Kontext Der Editionsphilologie_, edited by Katharina Krüger, 87–105. Editio / Beihefte, 40. Berlin, Boston: de Gruyter.

Burnard, Lou, Fotis Jannidis, Elena Pierazzo, and Malte Rehbein. 2010. “An Encoding Model for Genetic Editions.” Accessed March 25, 2019. http://www.tei-c.org/Activities/Council/Working/tcw19.html.

Cummings, James. 2018. “A World of Difference: Myths and Misconceptions About the TEI.” _Digital Scholarship Humanities_ 6:i63. doi:10.1093/llc/fqy071.

Efer, Thomas. 2016. “Graphdatenbanken Für Die Textorientierten E-Humanities.” Dissertation, Universität Leipzig.

Haentjens Dekker, Ronald, and David J. Birnbaum. 2017. “It's More Than Just Overlap: Text as Graph.” In _Proceedings of Balisage: The Markup Conference 2017_, edited by B. T. Usdin, Deborah A. Lapeyre, James D. Mason, C. M. Sperberg-McQueen, and Norman Walsh. Balisage Series on Markup Technologies: Mulberry Technologies, Inc.Rockville, Maryland.

Hofmeister, Wernfried, Astrid Böhm, and Helmut W. Klug. 2016. “Die Deutschsprachigen Marginaltexte Der Grazer Handschrift UB, Ms. 781 Als Interdisziplinärer Prüfstein Explorativer Revisionsforschung Und Editionstechnik.” _Editio_ 30 (1): 14–33. doi:10.1515/editio-2016-0002.

Hofmeister-Winter, Andrea. 2016. “Beredte Verbesserungen.” _Editio_ 30 (1): 1–13. doi:10.1515/editio-2016-0001.

Ide, Nancy, and Laurent Romary. 2006. “Representing Linguistic Corpora and Their Annotations.” In _Proceedings of the Fifth Language Resources and Evaluation Conference: LREC 2006_, edited by Nicoletta Calzolari, Khalid Choukri, Aldo Gangemi, Bente Maegaard, Joseph Mariani, Jan Odijk, and Daniel Tapias: Genua.

Ide, Nancy, and Keith Suderman. 2007. “GrAF: A Graph-Based Format for Linguistic Annotations.” In _Proceedings of the Linguistic Annotation Workshop: Held in Conjunction with ACL 2007_, edited by Association for Computational Linguistics, 1–8. https://www.aclweb.org/anthology/W07-1501. Accessed July 30, 2019.

Schmidt, Desmond, and Robert Colomb. 2009. “A Data Structure for Representing Multi-Version Texts Online.” _International Journal of Human-Computer Studies_ 67 (6): 497–514. doi:10.1016/j.ijhcs.2009.02.001.

Sperberg-McQueen, C. M., and Claus Huitfeldt. 2004. “GODDAG: A Data Structure for Overlapping Hierarchies.” In _Digital Documents: Systems and Principles_, edited by Peter King and Ethan V. Munson, 139–60. Berlin, Heidelberg: Springer.

TEI Consortium. 2013. “TEI P5: Guidelines for Electronic Text Encoding and Interchange.” Version 3.6.0. Accessed July 30, 2019. https://www.tei-c.org/Vault/P5/3.6.0/doc/tei-p5-doc/en/html/.

“The Stemmaweb Project: Tools and Techniques for Empirical Stemmatology.” 2012–. Accessed July 30, 2019. https://stemmaweb.net/.

W3C OWL Working Group. 2012. “OWL 2 Web Ontology Language: Document Overview (Second Edition).” W3C Recommendation 11 December 2012. Accessed June 08, 2018. https://www.w3.org/TR/owl2-overview/.
