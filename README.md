# flask-app-gpt (sentiment) api

## Template openai connect model
```python
import openai

# Set your OpenAI API key
openai.api_key = "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"

# Define the text you want to analyze or interact with
text = "ใจที่แตกสลายของนายปุณยากร สีนุชาติ"

# Make a request to the OpenAI GPT-3.5 API
response = openai.ChatCompletion.create(
    model="gpt-3.5-turbo-0125",
    messages=[
        # prompt
        {"role": "system", "content": "แต่งเนื้อเพลงให้หน่อย ขอแบบเพลงแนว rock และขอให้อ่านออกแบบไม่มั่ว พร้อมคอร์ดกีต้าร์ด้วย"},
        {"role": "user", "content": text}
    ]
)

# Extract the response text
response_text = response['choices'][0]['message']['content'].strip()

print("Response from GPT-3.5:", response_text)
```