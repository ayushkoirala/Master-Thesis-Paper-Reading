# `PROMPTSUM: PLANNING WITH MIXED PROMPTS FOR PARAMETER-EFFICIENT CONTROLLABLE ABSTRACTIVE SUMMARIZATION`

|Topic | PROMPTSUM: PLANNING WITH MIXED PROMPTS FOR PARAMETER-EFFICIENT CONTROLLABLE ABSTRACTIVE SUMMARIZATION|
|-------------|------------------------|
| Problems | Prompt tuning (PT) has been shown to be effective for language understanding tasks, it has not been effective for generation tasks such as summarization. This is because effective prompt design methods for generation tasks are still lacking|
|Solution |  The authors of the paper propose a new method called PromptSum. PromptSum combines PT with a multi-task objective and discrete entity prompts for abstractive summarization. The objective of this approach is to achieve strong summarization performance with parameter efficiency, data efficiency, and controllability. Specifically, the authors use discrete entity prompts to guide summarization and achieve a desirable double objective of higher quality and controllability in summary generation.|
| Paper Contribution |1. to propose using a mixture of discrete and soft prompts for generation tasks. We
empirically show its effectiveness on abstractive summarization.<br />2.our approach by introducing a multi-task prompt-tuning pre-training framework. <br />3. Propose the first light-weight controllable summarization model,
which shows impressive levels of controllability of the summary even with few-shot supervision.|

