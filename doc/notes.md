Preface
    Thanks
Abstract
Intro to thesis topic
    Context
    Motivation
    Goal
    Challenges
    Thesis structure
Intro to DT
    Prerequisites & definitions
        training, test set
        attributes, class label
        categorical vs numeric
        (internal) nodes vs leaves
        pure nodes
        validation metrics (acc, F1), cross val, ...
        see Excel
        ==> don't explain at length what target audience already knows!
    Why use?
        comprehensible, learning speed, classification speed, few hyperparams, missing values easy {kotsiantis2007supervised}
            TODO missing values fix?
        note: fuzzy algorithm names (versioning)
        redundant attributes?
        interdependent/correlated attributes?
        noise resistance? ~ overfitting
    Comparison to other ML algos
        works best on categorical features -> SVM, NN for numerical
    Scope
        Top down
        Classification
        Univariate
        In memory -> before big data era
        No ensembles
    Math
        axis-aligned hyperrectangles
        optimal tree: NP-Complete {npcomplete}
        big O's -> scikit docs
    Splitting heuristics
        leaf, binary/n-ary
        distance: gini {cart} | info theory {shannon1948mathematical}: entropy, IG, IGR | chi²
        not all that important {cart} -> stopping criteria!
            same for attribute selection -> TODO more details
    Stopping criteria
    Overfitting
        Early stopping
        Pruning -> comprehensibility
            non-exhaustive
                cost complexity pruning: {cart}
                REP: {quinlan1987simplifying}
                EBP: {?}
                pessimistic: {quinlan1987simplifying, c45}
                MDL: {quinlan1989inferring}
            easy to switch, but evaluate holistically
        greedy -> horizon
    Extensions
        Rules
            prune via rules
        Oblique (multivariate)
        Logic
    Ensembles
        Bagging
        Boosting
Software capabilities
    weka
    scikit
Methodology
    Datasets + description
    Architecture?
Results and discussion
    Pruning
        REP
        EBP
    Categorical attributes
        one hot encoding
Conclusion
    Retrospective
    Future work

Quinlan: ML -> focus on categorical
Breiman: statistics -> focus on numerical