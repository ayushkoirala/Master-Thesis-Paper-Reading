#1. Topic-Centric Unsupervised Multi-Document Summarization of Scientific and News Articles

#2. Paper Link : https://arxiv.org/pdf/2011.08072v1.pdf

| Topic | Topic-Centric Unsupervised Multi-Document Summarization of Scientific and News Articles |
| ---------------| --------------------------- |
| Problems |1. The increasing number of articles published in the research and media community has created a need for coherent, concise, informative, and grammatically correct summaries.<br />2. Abstractive summarization, which involves paraphrasing and fusing sentences to create new and informative summaries, poses challenges in capturing abstractive concepts shared among sentences across multiple documents.|
|Solution |The framework proposed in the paper consists of two phases: an extractive phase and an abstractive phase. In the extractive phase, a three-fold approach is followed: <br /> a. Core and peripheral articles are identified for each set of related articles.<br /> b. Clusters are instantiated using language units from the core article, and centroid-based clustering is performed to place language units from peripheral articles into the clusters.<br /> c. Language units within a cluster are fused using an enhanced Multi-Sentence Compression (MSC) technique, along with a novel algorithm, to maximize topical coverage and relevance.<br />In the abstractive summarization phase:<br />a. Abstractive Language Units (ALUs) are generated using GPT-2, a text generation model.<br />b. The generated ALUs are fused into an abstractive summary using MSC.|
