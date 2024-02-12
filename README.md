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
