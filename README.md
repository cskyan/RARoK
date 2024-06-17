# RARoK

<div align="center">![RARoK Introduction](figure/RARoK Introduction Method.jpg)</div>
## Abstract 
Although large language models (LLMs) perform impressively in natural language tasks, they face several challenges, such as incorporating new knowledge, generating accurate responses, and explaining their reasoning.  To address these issues, we propose a new approach called Retrieval-Augmented Reasoning on Knowledge (RARoK) that combines Chain of Thought (CoT) prompts with Retrieval-Augmented Generation (RAG) techniques.  By leveraging external information from knowledge graphs (KGs), RARoK iteratively corrects CoT to further optimize the model’s reasoning process.  The approach significantly outperforms the baseline in various Q&A tasks, especially in the medical domain.  Compared to the SOTA method, RARoK improves Hits@1 by 3.3% on the WebQSP dataset and improves Hits@1 and F1 scores by 18.6% and 10.4% on the CWQ dataset.  Experiments on the Knowledge Graph Q&A datasets and the Medical Q&A datasets show that our method has better reasoning and interpretability compared to vanilla LLMs and other retrieval-enhanced methods.
## Prerequisites

* Python packages can be installed with `pip install -r requirements.txt`

* `OpenAI_API_key` is required for the language model. You can get it from [OpenAI](https://beta.openai.com/signup/). 
```
export OPENAI_API_KEY="sk-******"
```

* You can also use the Huggingface API key for the language model. You can get it from [Huggingface](https://huggingface.co/join).

* You also need to prepare the `GOOGLE_API_KEY` for Google Search API. You can get it from [Google Cloud Platform](https://cloud.google.com/docs/authentication/getting-started).
```
export GOOGLE_API_KEY="********"
```