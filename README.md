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
Mixtral-Instruct
|            Tasks             |Version|Filter|n-shot|Metric|Value|   |Stderr|
|------------------------------|------:|------|------|------|----:|---|-----:|
|ger_rag_benchmark_chatml_task1|      1|none  |None  |acc   |0.956|±  |0.0065|
|ger_rag_benchmark_chatml_task3|      1|none  |None  |acc   |0.468|±  |0.0158|
|ger_rag_benchmark_chatml_task4|      1|none  |None  |acc   |0.597|±  |0.0155|
|ger_rag_benchmark_chatml_task5|      1|none  |None  |acc   |0.931|±  |0.0080|

03_04_mixtral_sft_ax_03
|            Tasks             |Version|Filter|n-shot|Metric|Value|   |Stderr|
|------------------------------|------:|------|------|------|----:|---|-----:|
|ger_rag_benchmark_chatml_task1|      1|none  |None  |acc   |0.986|±  |0.0037|
|ger_rag_benchmark_chatml_task3|      1|none  |None  |acc   |0.640|±  |0.0152|
|ger_rag_benchmark_chatml_task4|      1|none  |None  |acc   |0.611|±  |0.0154|
|ger_rag_benchmark_chatml_task5|      1|none  |None  |acc   |0.805|±  |0.0125|

03_04_mixtral_sft_rag_ax_02
|            Tasks             |Version|Filter|n-shot|Metric|Value|   |Stderr|
|------------------------------|------:|------|------|------|----:|---|-----:|
|ger_rag_benchmark_chatml_task1|      1|none  |None  |acc   |0.994|±  |0.0024|
|ger_rag_benchmark_chatml_task3|      1|none  |None  |acc   |0.465|±  |0.0158|
|ger_rag_benchmark_chatml_task4|      1|none  |None  |acc   |0.512|±  |0.0158|
|ger_rag_benchmark_chatml_task5|      1|none  |None  |acc   |0.846|±  |0.0114|

03_13_g3_mixtral_dpo_ax_02
|            Tasks             |Version|Filter|n-shot|Metric|Value|   |Stderr|
|------------------------------|------:|------|------|------|----:|---|-----:|
|ger_rag_benchmark_chatml_task1|      1|none  |None  |acc   |0.991|±  |0.0030|
|ger_rag_benchmark_chatml_task3|      1|none  |None  |acc   |0.501|±  |0.0158|
|ger_rag_benchmark_chatml_task4|      1|none  |None  |acc   |0.518|±  |0.0158|
|ger_rag_benchmark_chatml_task5|      1|none  |None  |acc   |0.858|±  |0.0110|

```
