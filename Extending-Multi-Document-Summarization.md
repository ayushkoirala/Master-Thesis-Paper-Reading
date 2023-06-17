#`Extending Multi-Document Summarization Evaluation to the Interactive Setting`

|Problem|Traditional information seeking tasks, such as search, question-answering, and multi-document summarization, typically follow a single-round input-output process, limiting the extent to which users can guide the information gathering process. While interactive settings have gained momentum in search and question-answering domains, interactive summarization systems that allow users to affect summary content have seen limited development and adoption. A key gap in this area is the lack of evaluation methodologies and benchmarks for meaningful comparison of interactive summarization systems.|
|Solution|The paper proposes an end-to-end evaluation framework for interactive summarization (INTSUMM) systems. The framework involves collecting real user sessions through controlled crowdsourcing. The sessions are then measured to generate absolute scores for system evaluation, enabling robust system comparison. The framework supports expansion-based interactive summarization, where the textual summary gradually expands in response to user interaction.<br />1. Evaluation Measures: The authors propose a set of automatic and manual evaluation measures for INTSUMM systems. These measures combine established notions in static summarization and interactive systems and utilize existing multi-document summarization datasets. Unlike static summarization, the evaluation measures in the interactive setting reflect the progress of information acquirement throughout the interaction, measuring the accumulating information gain with a recall metric.<br />2/Crowdsourced Session Collection Process: Adequate evaluation and comparison of INTSUMM systems require collecting realistic user sessions consistently. The paper describes a controlled crowdsourcing procedure designed to overcome the challenges of replicability and comparability in previous approaches. This procedure improves the reliability and accessibility of the evaluation process for researchers interested in interactive summarization research.|
|Methodology|1. Evaluation Setup: The INTSUMM system is evaluated based on multiple sessions conducted by human users. Each session consists of a set of documents to explore, an initial summary, and a sequence of user requests and system responses. The interactive summary is built incrementally through the interactions, resulting in a sequence of expanding snapshots.<br />2. Automatic Measures: To assess system performance, several automatic measures are used. These measures focus on capturing the information gained during the session. The following indicators are defined:Recall-by-Length Curve: A curve that shows the recall score of the summary snapshots at different word-lengths.<br />Area Under the Recall-Curve (AUC): A measure that quantifies the information gain by computing the area under the recall curve.<br />Score@Length: A metric that reports the system's effectiveness at specific word-lengths by using standard evaluation measures such as ROUGE F1.<br />These per-session indicators provide insights into the information gain and performance of the system during individual sessions. Aggregated indicators, such as the average recall curve, average AUC, and average Score@Length, are computed to evaluate the system's overall performance.<br />Human Ratings: Manual evaluation metrics are used alongside automatic measures to assess the quality of the summarization system. The following ratings are collected from users:<br />Rating of Initial Summary: Users rate the informativeness of the initial summary.<br />Rating of Information Gain: Users rate the usefulness of each interaction's response in adding new information.<br />Rating of System Responsiveness: Users rate how well the system responds to their requests throughout the session.<br />Usability Rating: Users rate the System's capabilities and ease of use using the UMUX-Lite questionnaire.<br />These ratings provide a more accurate assessment of the system's quality, although they require more resources and effort compared to automatic measures.|