SSF_Package.zip contains the package for installation in WEKA (version >= 3.7.1).

For installation:
-> Start weka as usually (e.g. java -jar weka.jar)
-> Go to Tools > Package Manager
-> Click in File/Url in the Unofficial box and Select the SSF_Package.zip file


To run SSF use the SSF Attribute Evaluator and S^3F use the S3F Attribute Evaluator.
For the search method you must use KMedoidsSampling.

Important: SSF ignores the class attribute if set in the loaded dataset.

Use the -S <num> parameter for SSF and S3F to indicate the strategy to select features from the induced clusters (0 -> select only medoids; 1-> select medoids and frontier)

For KMedoidSampling the following parameters are available:
-P <num> indicate the minimum number of attributes groups (k_min)
-Q <num> indicate the maximum number of attributes groups (k_max)
-N <num> number of repetitions for each value of k
-V <validationCriteria class> validation criteria used to assess the partitions quality
-D <distanceFunctionForSSF class> distance function (correlation) used to assess similarities between features

For validation criteria only the Simplified Silhouette is available in: weka.attributeSelection.ssf.validationCriteria.SimplifiedSilhouette

For distance functions (correalations) the possibilities are:
  weka.attributeSelection.ssf.distanceFunctions.AIR
  weka.attributeSelection.ssf.distanceFunctions.MaximalInformationCompressionIndex
  weka.attributeSelection.ssf.distanceFunctions.PearsonCorrelation
  weka.attributeSelection.ssf.distanceFunctions.SymmetricalUncertainty
  weka.attributeSelection.ssf.distanceFunctions.SymmetricalUncertaintySupervised

Note that the last (SymmetricalUncertaintySupervised - SU_s) must be used for S^3F.

For more information see the paper:
Thiago F. Covões, Eduardo R. Hruschka (2011). Towards Improving Cluster-Based Feature Selection with a Simplified Silhouette Filter. Information Sciences.


