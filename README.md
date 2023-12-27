# Natural-Language-Processing-with-SpaCy
Example of using the SpaCy library for natural language processing.
import spacy

# Load the English NLP model from SpaCy
nlp = spacy.load("en_core_web_sm")

# Process a text using SpaCy
text = "SpaCy is a powerful natural language processing library."
doc = nlp(text)

# Extract named entities from the text
named_entities = [(ent.text, ent.label_) for ent in doc.ents]

print("Named Entities:")
for entity in named_entities:
    print(f"{entity[0]} - {entity[1]}")
