# Layer-Skip

This repo contains a *single* patched file—`transformers/models/llama/modeling_llama.py`—that adds lightweight layer-skipping support to Llama models.  
Simply put: drop this file into your local **🤗 Transformers** installation (or put this repo on your `PYTHONPATH`), and you can benchmark the modified model with **lm-evaluation-harness**.

---

## Quick start

```bash
# 1. Clone
git clone https://github.com/Ethlake/Layer-skip.git
cd Layer-skip

# 2. Create an environment and install runtime deps
python -m venv .venv && source .venv/bin/activate
pip install torch transformers lm-eval        # tested with transformers ≥ 4.40 :contentReference[oaicite:0]{index=0}

# 3.Use the following command to evaluate models on various datasets (detailed information can be seen in official lm-evaluation-harness repositories)

python -m lm_eval \
  --model hf \
  --model_args "pretrained=meta-llama/Llama-2-7b" \
  --tasks arc_challenge \
  --device cuda




