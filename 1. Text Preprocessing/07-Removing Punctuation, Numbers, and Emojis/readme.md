import re

text = "Hello!!! NLP is 100% fun 😄👍."

# Remove punctuation, numbers, and emojis

clean_text = re.sub(r'[^A-Za-z\s]', '', text)

print("Clean Text:", clean_text)
