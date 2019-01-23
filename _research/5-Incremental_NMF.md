---
title: "Incremental Nonnegative Matrix Factorization (INMF)"
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
Test results verify the INMF's efficiency in dimension reduction and success in online factorization of large data sets.


### Supplementary Documents

* [Proof](INMF_conv_proof.pdf) of convergence for the update rules of INMF.
* Does NMF satisfies KKT complementarity condition at convergence? The answer is [here](KKT.pdf).

### Statistical Background Modeling in Video Surveillance

Background modeling in surveillance type of video is a good example to judge the dynamic content representation
performance of a factorization method.  This task requires representing the background scene by using a small
number of background frames and then updating this representation in such a way that dynamic content changes
influence the representation appropriately. These changes include entrance / leaving of an object into / from
the scene and variations in object motions.

Conventionally, a quantitative measure of the dynamic content representation capability is the reconstruction
error between the original frame and its reconstruction. It is expected to obtain a significant increase in the
error if there is a change in the scene while the error converges to zero for the background frames. Of course
this is true under the assumption that the representation of background is satisfactory.

Test results are reported to compare background modeling performances of batch-mode and incremental NMF in video
surveillance. Moreover, test results obtained by the incremental PCA are also given for comparison purposes. It
is shown that INMF outperforms the conventional batch-mode NMF in all aspects of dynamic background modeling.
Although object tracking performance of INMF and the incremental PCA are comparable, INMF is much more robust
to illumination changes.


### Publications

S.S. Bucak, B. Gunsel, "Online Video Scene Clustering by Competitive Incremental NMF," Signal Image and Video 
Processing: 1-17 , 2011.  [[code]](addthe.zip)

S.S. Bucak, B. Gunsel, "Incremental Subspace Learning via Non-negative Matrix Factorization," Pattern 
Recognition , vol 42(5), pp. 788-797, May 2009. [[code]](addthe.zip)

S.S. Bucak, B. Gunsel, "Incremental Clustering via Nonnegative Matrix Factorization," International Conference 
on Pattern Recognition (ICPR), Florida, USA, 2008. [[code]](addthe.zip)

Bucak, S.S., Gunsel, B., Gursoy O., "Incremental Non-negative Matrix Factorization for Dynamic background
Modelling," ICEIS 8th International Workshop on Pattern Recognition in Information Systems (PRIS), Funchal, Portugal, 12-13 June 2007.

Bucak, S.S., Gunsel, B., Gursoy O., "Gözetleme Videolarında Artımlı Negatif Olmayan matris Ayrıştırma ile
Arka Plan Modelleme (Turkish)," IEEE 15. İşaret İşleme ve İletişim Uygulamaları Kurultayı (SIU), Eskisehir, Turkey, 11-13 June 2007.

### Scene Change Detection and Video Content Representation

Aim of the video scene change detection task is to be able to detect the frames where scene changes take place. These
scene changes can be classified as "cuts" and "gradual changes." Clean cuts are sudden changes between the scenes.
In contrast, gradual changes, i.e., fade in/out, dissolve, wipe, etc., are generally longer and can be defined as
continuous transitions between two different video scenes. Obviously, detection of the gradual changes is a more
difficult task. Another difficulty in this task is avoiding false alarms which are likely to be caused by camera
and object movements or lighting variations.

In the literature a number of video scene change algorithms have been reported.  We have evaluated the potential use
of INMF in video scene change detection. The idea behind is that if the INMF accurately represents the scene content
and the dynamic changes, a significant increase in the reconstruction error should be detected at the scene change
frames. Thus, determination of a video scene change is done by examining the changes on the reconstruction errors
of the successive frames.

Tests are carried out on over 130000 (%24 of all the transitions were gradual) frames from the video clips recorded
in TRECVID database. In order to reduce computational complexity, the INMF has been performed on the DC images of each
frame.  Video scene change detection performance of the INMF is evaluated in terms of two criteria: "precision" and
"recall". Precision is defined as the ratio of correct matches to the total number of transitions reported. On the
other hand, recall is the number of correct matches divided by the total number of actual transitions in the video
sequence. Hence, precision gives clue about the system's false positive performance whereas recall is related to
false negative ratio. As it is shown in Table 1, the number of false alarms is small, detection rates for both
gradual transitions and cuts are high imposing that the INMF is a promising tool in content analysis.

It is concluded that the introduced incremental non-negative matrix factorization, with its ability to adapt the
conventional NMF's useful features to its incremental nature, is an efficient tool for modelling dynamic content
in video applications.  Currently we are working on derivation of sparse INMF which could be more beneficial to
have more localized, parts-based representations to increase robustness to lighting variations and motion.

**Table 1.** Scene change detection performance of  the INMF.

|                  | Cuts          | Graduals      | Total |
|------------------|---------------|---------------|-------|
|True Positives #  | 590           | 174           | 764   |
|False Negatives # | 42            | 28            | 70    |
|Recall            | 0.93          | 0.86          | 0.92  |
|False Positives # |               |               | 120   |
|Precision         |               |               | 0.86  |

### Publications

Bucak, S.S., Gunsel, B.," Video Content Representation by Incremental Non-negative Matrix Factorization,
" IEEE  International Conference on Image Processing (ICIP),  San Antonio, Texas, USA, 16-19 September 2007.

### Clustering via NMF

It has been shown that (Ding & Li, 2006) non-negative matrix factorization is related to K-means clustering.
After investigating this relationship and extending it to the incremental non-negative matrix factorization
(INMF) scheme, we aim to implement the clustering ability of NMF on video content representation task. Formerly,
we have been using reconstructing performance as a criterion in detecting scene changes for video content
representation tasks. We now investigate whether the performance of the INMF in this task could be improved
by adding and using its clustering feature. Our aim is to include the performance criteria  used in clustering
tasks into our project in order to obtain better decision criteria for scene change detection and key frame selection tasks.

Clustering approach of NMF could also be useful in understanding the nature of NMF. Our recent experiments have shown
that rank selection, clustering and sparseness are related in NMF implementations. Examining clustering performance
of the representations could be useful in determining the optimal rank. Hence, we are currently investigating the
relationship between rank and clustering, and working on finding optimal rank selection scheme based on clustering
performance criteria.
