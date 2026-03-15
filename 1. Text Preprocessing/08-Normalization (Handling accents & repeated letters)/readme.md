import unicodedata
import re

text = "Héelloo sooo cooool!!!"

# Remove accents

text = unicodedata.normalize('NFKD', text).encode('ASCII', 'ignore').decode('utf-8')

# Reduce repeated letters (e.g., sooo -> so)

text = re.sub(r'(.)\1{2,}', r'\1\1', text)

print("Normalized Text:", text)
