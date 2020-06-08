# PHI/TLG CD-ROM Documentation

When I was first writing [Diogenes](https://github.com/pjheslin/diogenes), I had no access to any documentation apart from the Beta Code manual which the TLG has always put on its website.  So all of the lower-level Diogenes code is the product of reverse engineering, which is why it is so poorly commented. (That is my excuse, at any rate.) I was figuring it out as I was going along, so I was never in a position to write definitive comments explaining what the code was doing.  Most of the comments, such as they are, express puzzlement rather than certainty.

After I released Diogenes, some people did send me scraps of documentation of the file formats, and I have kept these.  More recently I have been asked if I could share any documentation I have of the CD-ROM databases, so I have put what I have in this repository, on the assumption that these docs are so old no one will mind.  

Several of these TLG technical notes went up on the TLG website during the initial period that I was working on Diogenes and I was able to make some use of them, but they do not seem to be available anymore. The Beta Code manual is still [there](http://www.tlg.uci.edu/encoding/BCM.pdf). A couple of these files do not have dates or provenance; I do not remember where I got them.

My experience is that having the documentation was not that helpful.  After receiving some of this documentation, I did go back and reimplement one bit of Diogenes that I was particularly unsure about.  This was the code that searches for a particular citation and therefore needs to know if it has gone past that citation yet.  As far as I remember it, the new, revised code was much slower, and was just as susceptible to bugs, for it turned out that not all of the files adhered strictly to the specification.

The database format is highly ingenious, being adapted to a world in which the citation data had to be processed in hardware in order to be fast enough, and in which 8KB of RAM was a lot.  But for those reasons it is not that convenient to work with.

If you want to process the original databases yourself, consider whether this is really necessary.  One of the reasons I implemented XML export in Diogenes was to obviate the necessity of anyone ever going back to the original databases.  It would be so much easier just to work with the XML.

Other projects I know of that work with the raw databases are:

* [tlgu](http://tlgu.carmen.gr/)
* [Beta2Uni](https://cental.uclouvain.be/beta2uni/)
* [Hipparchia](https://github.com/e-gun/HipparchiaServer)
