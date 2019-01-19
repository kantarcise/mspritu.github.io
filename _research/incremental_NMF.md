---
title: "Incremental NMF"
collection: research
type: "Research"
permalink: /research/Incremental_NMF
#venue: "UC San Francisco, Department of Testing"
#date: 2012-03-02
#location: "San Francisco, California"
---


We have introduced an incremental non-negative matrix factorization (INMF) scheme in order to overcome
the difficulties that the conventional NMF has in online processing of large data sets. Unlike the conventional
NMF, with its incremental nature and weighted cost function, the introduced INMF successfully utilizes adaptability
to dynamic content changes with a low computational complexity.

The proposed scheme updates former representations by adding the effect of each new sample to the factorization incrementally, 
while the weighted cost function enablescontrolling the memorylessness of the factorizations. We have shown that the introduced 
subspace learning schemeis capable of imposing sparseness and smoothness to the factorization with the help of extra cost terms.
Testresults verify the INMF's efficiency in dimension reduction and success in online factorization of large data sets.
