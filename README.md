# kul-mai-thesis-report

Master's thesis report for the Advanced Master in Artificial Intelligence program at KU Leuven.

## Findings

* <http://scikit-learn.org/stable/modules/tree.html>
  * keep #feature low
  * no pruning -> set `max_depth`, `min_samples_split`, `min_samples_leaf`
  * complexity

* MKL (BLAS & LAPACK implementation) is enabled by default in anaconda

* Notes on multi-class
  * <http://scikit-learn.org/stable/modules/multiclass.html>
  * <https://github.com/scikit-learn/scikit-learn/issues/1781>
  * <https://github.com/scikit-learn/scikit-learn/issues/2451>

* Weka J48 options
  * seed -- The seed used for randomizing the data when reduced-error pruning is used.
  * =>unpruned -- Whether pruning is performed.
  * 0 confidenceFactor -- The confidence factor used for pruning (smaller values incur more pruning).
  * 0 numFolds -- Determines the amount of data used for reduced-error pruning.  One fold is used for pruning, the rest for growing the tree.
  * //numDecimalPlaces -- The number of decimal places to be used for the output of numbers in the model.
  * //batchSize -- The preferred number of instances to process if batch prediction is being performed. More or fewer instances may be provided.
  * 0 reducedErrorPruning -- Whether reduced-error pruning is used instead of C.4.5 pruning.
  * useLaplace -- Whether counts at leaves are smoothed based on Laplace.
  * doNotMakeSplitPointActualValue -- If true, the split point is not relocated to an actual data value. This can yield substantial speed-ups for large datasets with numeric   * attributes.
  * //debug -- If set to true, classifier may output additional info to the console.
  * 0 subtreeRaising -- Whether to consider the subtree raising operation when pruning.
  * //saveInstanceData -- Whether to save the training data for visualization.
  * =>binarySplits -- Whether to use binary splits on nominal attributes when building the trees.
  * //doNotCheckCapabilities -- If set, classifier capabilities are not checked before classifier is built (Use with caution to reduce runtime).
  * minNumObj -- The minimum number of instances per leaf.
  * useMDLcorrection -- Whether MDL correction is used when finding splits on numeric attributes.
  * collapseTree -- Whether parts are removed that do not reduce training error.
* Other Weka trees:
  * DecisionStump: max_depth=1 + boosting
  * HoeffdingTree: VFDT, online
  * J48: C4.5
  * LMT: logistic model trees (LR at leafs)
  * M5P: M5 model tree
  * RandomForest
  * RandomTree: RF(n_estimators=1) or random max_features
  * REPTree: fast learner with reduced error pruning
* Is code reused in RF, ExtraTrees, Gradient Boosted Trees, ...? -> yes
* Pruning algorithm applicable to regression trees?
* Pruning: slower learning, faster prediction
* Pruning
  1. IG = LT heuristic, but near leafs purity matters more again
  2. purity on sample != purity on population
     * unbiased estimate needed -> validation set ==> reduced error pruning
* Stopping criteria -> impure leaves -> predict_proba
  * excl. "out of attributes" -> majority class
* Laplace smoothing used for missing values
* Tree balance?
  * balanced = faster
  * linear = easier to interpret (if/else)?

## Timing

* 1ECTS = 25-30h
* 15ECTS = 375-450h
* Time frame: November-May (7 months)
* 70% preparation, literature, programming, experiments: 262-315h in November-March
* 30% writing, preparing presentation: 113-135h in April-May

## Milestones

* `2017-10-02` First thesis topics online
* `2017-10-24` Thesis meeting 1
* `2017-10-29` - `2017-10-31` Unavailable (business trip)
* `2017-10-30` Formal thesis topic submission deadline
* `2017-11-13` - `2017-11-18` Unavailable (business trip)
* `2017-12-24` - `2018-01-02` Unavailable (holidays)
* `2018-01-30` Thesis meeting 2
* `2018-02-13` Intermediate presentation
* `2018-06-08 14h00` Thesis submission deadline
  * N physical copies @ Secretariat CS (N = number of jury members + 1 (library) + 1 (self))
  * Digital copy @ <https://eng.kuleuven.be/english/students/master-thesis/masters-thesis/digital-masters-thesis-1>
* `2018-06-27` - `2018-07-02` Defense
* `2018-07-?? 15h00` Deliberation
* `2018-07-?? 16h00` Proclamation & reception @ Arenberg Castle <https://wms.cs.kuleuven.be/cs/opleidingen/master-artificial-intelligence/MAI_SIP/proclamation-dates>

---

* `2018-08-17 14h00` Thesis submission deadline
* `2018-09-05`-`2018-09-10` Defense
* `2018-09-?? 15h00` Deliberation
* `2018-09-?? 16h00` Proclamation & reception @ Arenberg Castle