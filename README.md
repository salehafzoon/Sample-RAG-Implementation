# Sample RAG Implementation
![Python](https://img.shields.io/badge/Python-Compatible-green.svg)

Features:
- Simple domain knowledge included
- Medical report cases as documents
- Automatic loading and saving LLMs
- Loading local LLM capability
- Included LLMs:
  - Mistral 7b
  - PHI-2


## Authenitcal token setup for using Hugging face and OpenAI LLMs
Windows:
```bash
$env:HF_TOKEN= "hugging_face_token"
$env:OpenAI_TOKEN= "open_ai_token"
```
MacOS:
```bash
export HF_TOKEN="hugging_face_token"
export OPENAI_TOKEN="open_ai_token"
```

LLM response generation comparison (on RTX 3060 GPU):

| Model      | response Time  | RAM Usage | Sample Output                      |
|------------|------------|-----------|------------------------------------|
| PHI-2      | 42 seconds | 3 GB      | "Yes, it is a serious symptom. The score is 0.7." |
| Mistral-7b | 5 minutes | 19 GB     | "answer"                           |


## Getting Started

#### 1. Clone and Install

```bash
# Clone the repo

git clone https://github.com/salehafzoon/Sample-RAG-Implement   
```
