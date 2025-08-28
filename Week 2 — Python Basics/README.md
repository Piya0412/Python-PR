week-02-python-basics/day08_loops.py

# Day 8: Python Loops
files = ["day01_file_ops.sh", "day02_grep_find.sh", "day03_permissions.sh"]
for f in files:
    print("Processed:", f)


week-02-python-basics/day09_file_read.py

# Day 9: File Handling
with open("sample.txt", "w") as f:
    f.write("Generative AI is exciting!\n")

with open("sample.txt", "r") as f:
    for line in f:
        print(line.strip())


week-02-python-basics/day10_json_config.py

# Day 10: JSON Parsing
import json

config = '{"project": "GenAI", "days": 30}'
data = json.loads(config)
print("Project:", data["project"], "Duration:", data["days"])


week-02-python-basics/day11_hf_api.py

# Day 11: Hugging Face API
import requests

API_URL = "https://api-inference.huggingface.co/models/facebook/bart-large-cnn"
headers = {"Authorization": "Bearer YOUR_HF_TOKEN"}

res = requests.post(API_URL, headers=headers, json={"inputs": "Generative AI deployment is transforming cloud apps."})
print(res.json())


week-02-python-basics/day12_virtualenv.md

# Day 12: Python Virtual Environment

```bash
python3 -m venv venv
source venv/bin/activate
pip install requests boto3 streamlit



### `week-02-python-basics/day13_logging.py`
```python
# Day 13: Logging
import logging

logging.basicConfig(level=logging.INFO)
logging.info("Starting practice project")
logging.warning("This is just a test warning")
logging.error("This is a simulated error")


week-02-python-basics/day14_text_summary.py

# Day 14: Mini Summarizer
from transformers import pipeline

summarizer = pipeline("summarization", model="facebook/bart-large-cnn")
text = "Generative AI allows machines to create human-like content such as text, images, and speech."
print(summarizer(text, max_length=30, min_length=10, do_sample=False))
