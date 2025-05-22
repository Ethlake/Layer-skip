# Layer-Skip

This repo contains a *single* patched file—`transformers/models/llama/modeling_llama.py`—that adds lightweight layer-skipping support to Llama models.  
Simply put: drop this file into your local **🤗 Transformers** installation (or put this repo on your `PYTHONPATH`), and you can benchmark the modified model with **lm-evaluation-harness**.

---





