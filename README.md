# Sample RAG Implementation
![Python](https://img.shields.io/badge/Python-Compatible-green.svg)
![OpenAI](https://img.shields.io/badge/OpenAI-412991.svg?style=flat-square&logo=OpenAI&logoColor=white")
[![Model on HF](https://huggingface.co/datasets/huggingface/badges/resolve/main/model-on-hf-md.svg)](https://huggingface.co/models)
![Pytorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)


  
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
Sample prompt:
```
Here is some additional professional health knowledge that can help you better analyze the report:
----------------------------------------------------------------------
<Domain Knowledge>
----------------------------------------------------------------------
This is a patient’s medical record. Context information:
----------------------------------------------------------------------
<Medical report>
----------------------------------------------------------------------
Given the context and health knowledge, answer the below question by only one answer in JSON format with only one floating point number between 0 and 1 that is “score”. :
Does the person described in the case have Hunger symptoms? Do you think it is serious?
The rule of the JSON answer: 0-0.2 is mild or none, 0.3-0.6 is moderate, and above 0.7 is severe.

```
LLM sample response generation comparison with ground truth score as 0.2 (on RTX 3060 GPU):

| Model      | Response Time  | RAM Usage* | Sample Output                      |
|------------|------------|-----------|------------------------------------|
| PHI-2      | 38 seconds | 3 GB      | The answer: {"score": 0.5} |
| Mistral-7b | 4 minutes  | 19 GB     | The answer is: {"score": 0.3} |

\* System RAM usage, not GPU memory.

## Getting Started

#### 1. Clone and Install

```bash
# Clone the repo

git clone https://github.com/salehafzoon/Sample-RAG-Implement   
```
