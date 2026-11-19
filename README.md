# lens-models

Model files that the LENS desktop app downloads once, at first-run setup, after the user agrees.
Each model is a release; the app verifies every file's SHA-256 before using it.

| Release tag | Contents | Licence |
|---|---|---|
| `siglip2-l16-256-fp16-v1` | **Default text-search model.** OpenCLIP `ViT-L-16-SigLIP2-256` (`webli`) exported to ONNX fp16: `image.onnx`, `text.onnx`, `tokenizer.json`, `model_info.json` (includes the tuned relevance cut-off) | Apache-2.0 (Google SigLIP 2 weights) |
| `clip-vitl14-laion2b-fp16-v1` | Smaller optional alternative. OpenCLIP ViT-L/14 (`laion2b_s32b_b82k`) exported to ONNX fp16: `image.onnx`, `text.onnx`, `tokenizer.json`, `model_info.json` | MIT (OpenCLIP / LAION weights) |
| `buffalo_l-v1` | `model_info.json` only | — |

The face models (InsightFace `buffalo_l`: `det_10g.onnx`, `w600k_r50.onnx`) are **not** rehosted
here. Their weights are for non-commercial research use only, so LENS downloads them directly from
the official InsightFace release (`deepinsight/insightface`, tag `v0.7`, `buffalo_l.zip`) and checks
the zip's SHA-256.
