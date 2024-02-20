# LLM-Chatbot-with-Financial-Sentiment-Analysis

LLM chat bot with Financial sentiment analysis using by OpenVINO

Based on https://github.com/openvinotoolkit/openvino_notebooks#-ai-trends---notebook

![](https://github.com/Pooja-B/LLM-Chatbot-with-Financial-Sentiment-Analysis/blob/main/demo_LLM.gif)


We will further integrate a Financial Sentiment Analysis using Prosus/FinBert model.

LLM chatbot integrated with sentiment analysis offers a myriad of benefits ranging from personalized customer experiences to real-time market insights and efficient risk management
Sentiment analysis is a very important business KPI in Finance Industry. Many enterprises take important decisions based on sentiment analysis of customers
By analyzing user interactions and sentiment analysis results, financial institutions gain valuable insights into user preferences, market trends, and customer sentiment. These data-driven insights can inform product development, marketing strategies, and business decision-making, helping financial institutions stay competitive and responsive to changing market dynamics.

We will use RedPajama-INCITE-Chat-3B-v1 . This Model is capable of reasoning, multi-turn conversation, knowled,ge and generative answersIt is f
Free to use commercially(LLaMA 2 : Custom Free if you have under 700M users and you cannot use LLaMA outputs to train other LLMs besides LLaMA and its derivativeThe s)
Chat model is made available on OpenChatKit, which provides functionalities to further fine-tune the chat model and customize it for a specific application.g)

FinBERT is a pre-trained NLP model to analyze sentiment of financial text. It is built by further training the BERT language model in the finance domain, using a large financial corpus and thereby fine-tuning it for financial sentiment classification. Financial PhraseBank by Malo et al. (2014) is used for fine-tuning. For more details, please see the paper FinBERT: [Financial Sentiment Analysis with Pre-trained Language Models](https://arxiv.org/abs/1908.10063).

The model will give softmax outputs for three labels: positive, negative or neutral.Sentiment Analysis Chatbots in the finance industry offer numerous benefits to both financial institutions and users.

## Weight Compression
We will compress the model using NNCF. Weight compression provides a solid inference performance improvement which is on par with the performance of the full model quantization while reducing the size of LLMs. 
Neural Network Compression Framework (NNCF) provides weight quantization to 8 and 4-bit integer data types as a compression method primarily designed to optimize LLMs. 

LLMs require extensive memory to store the weights during inference, can benefit from weight compression in the following ways:
Enabling the inference of exceptionally large models that cannot be accommodated in the memory of the device;
Improving the inference performance of the models by reducing the latency of the memory access when computing the operations with weights, for example, Linear layers.

## Benchmarking Results 
Generative AI benchmarks on Intel CPU-only



![image](https://github.com/Pooja-B/LLM-Chatbot-with-Financial-Sentiment-Analysis/assets/9071192/7c9d5893-f9ce-4e1d-a36e-f8db51b29ede)


### Detailed benchmark reports are included in Benchmark folder for reference. 


![alt text](https://github.com/Pooja-B/LLM-Chatbot-with-Financial-Sentiment-Analysis/blob/main/SentimentAnalysisLLMChatbot.png)
