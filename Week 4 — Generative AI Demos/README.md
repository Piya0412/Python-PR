week-04-genai-demos/day22_streamlit_intro.py

import streamlit as st
st.title("Hello Generative AI 🚀")
st.write("Day 22: My first Streamlit app")


week-04-genai-demos/day23_summarizer_app.py

import streamlit as st, requests

st.title("AI Summarizer")
txt = st.text_area("Enter text:")

if st.button("Summarize"):
    API_URL = "https://api-inference.huggingface.co/models/facebook/bart-large-cnn"
    headers = {"Authorization": "Bearer YOUR_HF_TOKEN"}
    res = requests.post(API_URL, headers=headers, json={"inputs": txt})
    st.success(res.json()[0]['summary_text'])


week-04-genai-demos/day24_bedrock_textgen.py

# Day 24: AWS Bedrock text generation (pseudo-code)
import boto3

bedrock = boto3.client("bedrock-runtime")
response = bedrock.invoke_model(
    modelId="anthropic.claude-v2",
    contentType="application/json",
    body='{"prompt": "Write a poem about cloud computing"}'
)
print(response["body"].read())


week-04-genai-demos/day25_auth_cognito.md

# Day 25: AWS Cognito Authentication

1. Create user pool
2. Enable sign-in with email
3. Protect API Gateway with Cognito


week-04-genai-demos/day26_ollama_inference.md

# Day 26: Ollama local LLM inference

```bash
ollama run llama2 "Explain Generative AI"



### `week-04-genai-demos/day27_polly_tts.py`
```python
# Day 27: Amazon Polly text-to-speech
import boto3

polly = boto3.client("polly")
res = polly.synthesize_speech(Text="Generative AI with AWS is amazing", OutputFormat="mp3", VoiceId="Joanna")

with open("speech.mp3", "wb") as f:
    f.write(res["AudioStream"].read())
print("Saved speech.mp3")


week-04-genai-demos/day28_cloudwatch_logs.md

# Day 28: CloudWatch Logs

```bash
aws logs create-log-group --log-group-name genai-app
aws logs create-log-stream --log-group-name genai-app --log-stream-name stream1



### `week-04-genai-demos/day29_chatbot_app.py`
```python
import streamlit as st, requests

st.title("GenAI Chatbot")
msg = st.text_input("You:")
if st.button("Send"):
    res = requests.post(
      "https://api-inference.huggingface.co/models/facebook/blenderbot-400M-distill",
      headers={"Authorization": "Bearer YOUR_HF_TOKEN"},
      json={"inputs": msg})
    st.write("Bot:", res.json()[0]["generated_text"])


week-04-genai-demos/day30_capstone.md

# Day 30: Capstone Project 🚀

Final project:
- Backend: AWS Lambda + SageMaker
- Frontend: Streamlit chatbot
- Infra: CloudFormation + S3 logging

Goal → Deploy a **Generative AI chatbot** with secure API & UI.


