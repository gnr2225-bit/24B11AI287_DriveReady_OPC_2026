# Day 1 – How LLMs Work and Your First API Call

## Objective
To understand how Large Language Models (LLMs) work and make the first API call using the Groq API.

## Tools Used
- Python
- Google Colab
- Groq API
- OpenAI Python library

## Tasks Completed
1. Installed the OpenAI Python library.
2. Connected to the Groq API using an API key.
3. Made the first API call.
4. Created a chatbot for Sweet Crumbs Home Bakery.

## Experiments

### Experiment 1: Temperature
Compared temperature values 0.2 and 1.2 to observe response creativity.

**Observation:** Lower temperature gives more predictable responses, while higher temperature gives more varied and creative responses.

### Experiment 2: Hallucination
Tested whether the AI invents information when business facts are missing.

**Observation:** The AI used the fallback response instead of making unsupported delivery claims.

### Experiment 3: No Memory
Tested separate API calls and conversation history.

**Observation:** Separate calls do not automatically remember previous messages. Providing conversation history helps the AI remember information.

### Experiment 4: Token Usage
Compared prompt token usage for English and Telugu questions.

**Observation:**
- English: 82 prompt tokens
- Telugu: 94 prompt tokens

### Experiment 5: Your Business
Created a chatbot for a Smart Stationery Store and tested three customer questions.

## Conclusion
Learned how to connect to an LLM using an API and explored temperature, hallucinations, memory, and token usage.