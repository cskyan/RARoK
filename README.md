# RARoK:Retrieval-Augmented Reasoning on Knowledge for Medical Question Answering
<div align=center><img src="figure/RARoK.jpg" width = "60%" height="60%"></div>

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

## Run RARoK
As the chatdoctor5k dataset for example. First, you need to create a Blank Sandbox on [https://sandbox.neo4j.com/](https://sandbox.neo4j.com/), click "connect via drivers", find your url and user password. Then replace the following parts in MindMap.py:
```
uri = "Your_url"
username = "Your_user"     
password = "Your_password"
```
Note that the data of CMCKG is too large, and it will take about two days to wait. We recommend clicking "extend your project" in neo4j sandbox. But don't worry, the EMCKG used by chatdoctor5k will be ready to build on your facility in no time.
Then, don't forget to replace your openai_key in MindMap.py.

```
python RARoK.py
```

## Acknowledgements

Our code  is based on [MindMap: Knowledge Graph Prompting Sparks Graph of Thoughts in Large Language Models](https://github.com/wyl-willing/MindMap/tree/main), the paper was proposed by Wen Yilin, Wang Zifeng and Sun  Jimeng In Proceedings of the 62nd Annual Meeting of the Association for Computational Linguistics.
