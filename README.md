# German RAG Benchmark

## Example

```bash
lm_eval --model hf \
    --model_args pretrained=TinyLlama/TinyLlama-1.1B-Chat-v1.0 \
    --tasks ger_rag_benchmark \
    --device cuda:0 \
    --batch_size 8

lm_eval --model hf \
    --model_args pretrained=DiscoResearch/DiscoLM_German_7b_v1 \
    --tasks ger_rag_benchmark \
    --device cuda:0 \
    --batch_size 1
```

## Results (ger_rag_benchmark_chatml)

```text
vllm (pretrained=/mnt/azureml/xxx/base_models/Mixtral-Instruct,tensor_parallel_size=2,dtype=auto,gpu_memory_utilization=0.8,data_parallel_size=1), gen_kwargs: (None), limit: None, num_fewshot: None, batch_size: auto
|            Tasks             |Version|Filter|n-shot| Metric |Value|   |Stderr|
|------------------------------|------:|------|------|--------|----:|---|-----:|
|ger_rag_benchmark_chatml_task1|      1|none  |None  |acc     |0.947|±  |0.0071|
|                              |       |none  |None  |acc_norm|0.947|±  |0.0071|
|ger_rag_benchmark_chatml_task2|      1|none  |None  |acc     |0.282|±  |0.0142|
|                              |       |none  |None  |acc_norm|0.282|±  |0.0142|
|ger_rag_benchmark_chatml_task3|      1|none  |None  |acc     |0.474|±  |0.0158|
|                              |       |none  |None  |acc_norm|0.474|±  |0.0158|
```

## Results (ger_rag_benchmark)

```text
hf (pretrained=TinyLlama/TinyLlama-1.1B-Chat-v1.0), gen_kwargs: (None), limit: None, num_fewshot: None, batch_size: 8
|         Tasks         |Version|Filter|n-shot| Metric |Value|   |Stderr|
|-----------------------|------:|------|-----:|--------|----:|---|-----:|
|ger_rag_benchmark_task1|      1|none  |     0|acc     |0.169|±  |0.0119|
|                       |       |none  |     0|acc_norm|0.169|±  |0.0119|
|ger_rag_benchmark_task2|      1|none  |     0|acc     |0.320|±  |0.0148|
|                       |       |none  |     0|acc_norm|0.320|±  |0.0148|
|ger_rag_benchmark_task3|      1|none  |     0|acc     |0.241|±  |0.0135|
|                       |       |none  |     0|acc_norm|0.241|±  |0.0135|

hf (pretrained=microsoft/phi-2), gen_kwargs: (None), limit: None, num_fewshot: None, batch_size: 2
|         Tasks         |Version|Filter|n-shot| Metric |Value|   |Stderr|
|-----------------------|------:|------|-----:|--------|----:|---|-----:|
|ger_rag_benchmark_task1|      1|none  |     0|acc     |0.237|±  |0.0135|
|                       |       |none  |     0|acc_norm|0.237|±  |0.0135|
|ger_rag_benchmark_task2|      1|none  |     0|acc     |0.240|±  |0.0135|
|                       |       |none  |     0|acc_norm|0.240|±  |0.0135|
|ger_rag_benchmark_task3|      1|none  |     0|acc     |0.249|±  |0.0137|
|                       |       |none  |     0|acc_norm|0.249|±  |0.0137|

hf (pretrained=DiscoResearch/DiscoLM_German_7b_v1), gen_kwargs: (None), limit: None, num_fewshot: None, batch_size: 4
|         Tasks         |Version|Filter|n-shot| Metric |Value|   |Stderr|
|-----------------------|------:|------|------|--------|----:|---|-----:|
|ger_rag_benchmark_task1|      1|none  |None  |acc     |0.253|±  |0.0138|
|                       |       |none  |None  |acc_norm|0.253|±  |0.0138|
|ger_rag_benchmark_task2|      1|none  |None  |acc     |0.264|±  |0.0139|
|                       |       |none  |None  |acc_norm|0.264|±  |0.0139|
|ger_rag_benchmark_task3|      1|none  |None  |acc     |0.253|±  |0.0138|
|                       |       |none  |None  |acc_norm|0.253|±  |0.0138|

vllm (pretrained=/mnt/azureml/xxx/base_models/Mixtral-Instruct,tensor_parallel_size=2,dtype=auto,gpu_memory_utilization=0.8,data_parallel_size=1), gen_kwargs: (None), limit: None, num_fewshot: None, batch_size: auto
|         Tasks         |Version|Filter|n-shot| Metric |Value|   |Stderr|
|-----------------------|------:|------|------|--------|----:|---|-----:|
|ger_rag_benchmark_task1|      1|none  |None  |acc     |0.261|±  |0.0139|
|                       |       |none  |None  |acc_norm|0.261|±  |0.0139|
|ger_rag_benchmark_task2|      1|none  |None  |acc     |0.276|±  |0.0141|
|                       |       |none  |None  |acc_norm|0.276|±  |0.0141|
|ger_rag_benchmark_task3|      1|none  |None  |acc     |0.237|±  |0.0135|
|                       |       |none  |None  |acc_norm|0.237|±  |0.0135|

vllm (pretrained=/mnt/azureml/xxx/base_models/Nous_Hermes_Mixtral,tensor_parallel_size=2,dtype=auto,gpu_memory_utilization=0.8,data_parallel_size=1), gen_kwargs: (None), limit: None, num_fewshot: None, batch_size: auto
|         Tasks         |Version|Filter|n-shot| Metric |Value|   |Stderr|
|-----------------------|------:|------|------|--------|----:|---|-----:|
|ger_rag_benchmark_task1|      1|none  |None  |acc     |0.177|±  |0.0121|
|                       |       |none  |None  |acc_norm|0.177|±  |0.0121|
|ger_rag_benchmark_task2|      1|none  |None  |acc     |0.327|±  |0.0148|
|                       |       |none  |None  |acc_norm|0.327|±  |0.0148|
|ger_rag_benchmark_task3|      1|none  |None  |acc     |0.235|±  |0.0134|
|                       |       |none  |None  |acc_norm|0.235|±  |0.0134|

vllm (pretrained=/mnt/azureml/xxx/base_models/SauerkrautLM_Mixtral,tensor_parallel_size=2,dtype=auto,gpu_memory_utilization=0.8,data_parallel_size=1), gen_kwargs: (None), limit: None, num_fewshot: None, batch_size: auto
|         Tasks         |Version|Filter|n-shot| Metric |Value|   |Stderr|
|-----------------------|------:|------|------|--------|----:|---|-----:|
|ger_rag_benchmark_task1|      1|none  |None  |acc     |0.288|±  |0.0143|
|                       |       |none  |None  |acc_norm|0.288|±  |0.0143|
|ger_rag_benchmark_task2|      1|none  |None  |acc     |0.229|±  |0.0133|
|                       |       |none  |None  |acc_norm|0.229|±  |0.0133|
|ger_rag_benchmark_task3|      1|none  |None  |acc     |0.240|±  |0.0135|
|                       |       |none  |None  |acc_norm|0.240|±  |0.0135|
```
