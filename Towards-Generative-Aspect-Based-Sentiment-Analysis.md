1. Towards Generative Aspect-Based Sentiment Analysis https://aclanthology.org/2021.acl-short.64.pdf

| 1. Topic | Towards Generative Aspect-Based Sentiment Analysis |
|-----|--------------------------|
| 2. Problem | Most existing methods in Aspect-based Sentiment Analysis (ABSA) are discriminative and ignore the rich label semantics in ABSA problems. They also require extensive task-specific designs. (In a discriminative approach, the model is trained to learn a mapping from the input text to a set of predefined sentiment labels (e.g., positive, negative, neutral) for each aspect. The model then uses this mapping to make predictions about the sentiment of new, unseen text.)|
| 3. Solution | The authors propose a new approach to tackle various ABSA tasks in a unified generative framework. Two types of paradigms, annotation-style and extraction-style modeling, are designed to enable the training process by formulating each ABSA task as a text generation problem. The proposed generative approach achieves new state-of-the-art results in almost all cases and has a strong generality that can be easily adapted to arbitrary ABSA task without additional task-specific model design. |
|  4. Methodology | Generative ABSA(GAS) : <br /> 4.1  ABSA with Generative Paradigm <br /> 
* Aspect Opinion Pair Extraction (AOPE): [aspect / opinion] Example: Salad were fantastic, our server was also very helpful. (Annotation-style): [Salads / fantastic] were fantastic here, our [server / helpful] was also very helpful. Target (Extraction-style): (Salads,fantastic); (server, helpful)
* Unified ABSA (UABSA) : [aspect /sentiment polarity] For example: (Salad,positive) and (server,positive)
* Aspect Sentiment Triplet Extraction(ASTE): (aspect,opinion,sentiment polarity) triplets. For example: Input: The Unibody construction is solid, sleek and beautiful.
Target (Annotation-style): The [Unibody construction / positive | solid, sleek, beautiful] is solid, sleek and beautiful. Target (Extraction-style): (Unibody construction, solid, positive); (Unibody construction,sleek, positive); (Unibody construction, beautiful, positive) <br />
