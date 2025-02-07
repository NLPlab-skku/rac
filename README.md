# RAC: Retrieval-augmented Conversation Dataset for Open-domain Question Answering in Conversational Settings (EMNLP 2024 Industry Track)

* November 2024: The dataset is released
* October 2024: The paper is accepted to EMNLP 2024 Industry Track

## Task Description
RAC aims to generate human-like respones requiring external knowledge to given user questions in conversations. Hence, the dataset covers two well-known tasks of which are conversational search and retrieval-augmented generation (RAG); query rewriting for retrieval purpose and response generation based on retrieved knowledge.

## Dataset
RAC is a Korean dataset contains 8.6k turns within 1.2k conversations. We built the dataset based on Knowledge-retrieval Conversation dataset which is released by Korea government in [AI-hub](https://www.aihub.or.kr/aihubdata/data/view.do?currMenu=&topMenu=&aihubDataSe=data&dataSetSn=71304). For each question in a conversation, we rewrote a search query as the question is often inappropriate for retrieving relevant passages due to its inherit limitation such as coreference or ellipsis. In addition, since original dataset only provides URLs of relevant passages, about 1.3M passages were collected to construct knowledge base for retrieval purpose. To extend the number of relevant passages following the real-world scenario, we retrieved passages using humane rewrite queries by Elastic Search and annotated relevance of the retrieved passages ranked within Top-5. Finally, each data consists of:

```
{
  'cid': "BK22003140",
  'qid': 6036,
  'topic': "미용과 건강",
  'question':  "어떤 음식을 먹어야 루테인을 풍부하게 보충할 수 있을까?",
  'query':  "루테인 식품",
  'response': "보통 아욱, 배추, 시금치, 양상추, 늙은 호박, 계란 노른자, 민들레 잎과 같은 음식에 풍부하지.",
  'history': [
    {
      'question': "요즘 비타민을 챙겨 먹고 있는데 루테인이 그렇게 좋다며?",
      'response': "응, 루테인은 시력 저하를 방지해. 왜냐하면 ..."
    },
    ...
  ],
  'reference_text': [
    "루테인은 아욱, 배추, 시금치, 양상추, 늙은 호박, 계란 노른자, 민들레 잎, 그리고 딜이나 쪽파 같은 허브에 풍부하다.",
    ...
  ],
  'relevant_passages': {
    'gold': [54389],
    'annotated': [556754, ...]
  }
}
```

The passage collection can be downloaded at [here]([https://works.do/587X3HB](https://works.do/xRtd46w)).


## Baseline

### Will be updated soon.
