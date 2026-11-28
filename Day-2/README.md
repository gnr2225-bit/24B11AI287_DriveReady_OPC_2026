# Day 2 -- Prompts, Memory and Python Agents

## Overview

This folder contains the Day 2 Python exercises for the AI Agents
workshop. The activities practise writing prompts, using few-shot
examples, requesting JSON, managing chat history, and creating a simple
business chatbot.

## Learning objectives

-   Understand the roles of `system`, `user`, and `assistant` messages.
-   Structure a system prompt using role, facts, rules, and output
    format.
-   Compare zero-shot and few-shot prompting.
-   Classify customer messages using a fixed set of labels.
-   Request structured JSON and parse it into a Python dictionary.
-   Maintain a short conversation history and limit the number of turns.
-   Use a Python dictionary and a function in a simple chatbot.

## Requirements

-   Python 3
-   The `openai` Python package
-   An API key configured in the environment
-   The `client` object created during Day 1

If the package has not been installed, run:

``` python
!pip install openai
```

Use the same `client` setup and model name from Day 1. Do not paste an
API key directly into a notebook that may be shared.

## Day 2 activities

### 1. Prompt parts

Run the same customer question twice: - First, use a prompt without the
RULES section. - Next, restore the RULES section and ask the same
question again.

Compare the two replies. The purpose is to see how explicit rules guide
the assistant and prevent unsupported promises.

### 2. Few-shot classifier

Create a classifier for customer messages with three labelled
examples: - `order` - `question` - `complaint`

Test the classifier with five new messages. The model should return one
label for each message. Few-shot examples demonstrate the expected
answer format; they do not train or permanently modify the model.

### 3. JSON output

Ask the assistant to extract an order using these fields: - `name` -
`item` - `qty` - `date` - `eggless`

Request JSON only, then parse the response with `json.loads()` inside a
`try/except` block.

### 4. Conversation memory

Set `MAX_TURNS = 2`. Tell the chatbot your name, continue the
conversation for three turns, and then ask it to recall your name.
Observe what happens when older messages are removed from the history
sent to the model.

### 5. Your own business chatbot

Adapt the example for a business of your choice: - Store the menu or
product catalogue in a Python dictionary. - Write at least one function
with a docstring. - Create a system prompt describing the business and
its rules.

## How to run

1.  Open the Day 2 notebook in Google Colab or another Python
    environment.
2.  Make sure the Day 1 API client setup has already been run.
3.  Run each activity in its own cell, in order.
4.  Check the printed model responses. Actual wording may vary between
    runs.
5.  Save screenshots of the code and output if they are required for
    submission.

## Key concepts

  -----------------------------------------------------------------------
  Concept                             Meaning
  ----------------------------------- -----------------------------------
  System message                      Instructions that define the
                                      assistant's role and behaviour

  User message                        The customer's input

  Assistant message                   The model's reply

  Zero-shot prompting                 Instructions without worked
                                      examples

  Few-shot prompting                  Instructions plus a few
                                      input/output examples

  JSON                                Structured data that programs can
                                      parse

  Chat history                        Earlier messages included as
                                      context for a reply

  `try/except`                        Handles errors without stopping the
                                      whole program
  -----------------------------------------------------------------------

## Notes

-   Keep the model's output format consistent when your Python code
    needs to process it.
-   Use a low temperature for more consistent classification.
-   A few-shot prompt provides examples for the current request; it is
    not model training.
-   Do not assume the assistant knows delivery times or other business
    details unless they are provided in the prompt.
-   Keep API keys private.

## Completion checklist

-   [ ] Compared the prompt with and without RULES.
-   [ ] Classified five new customer messages using three examples.
-   [ ] Requested order details as JSON and parsed the result.
-   [ ] Tested memory with `MAX_TURNS = 2`.
-   [ ] Created a chatbot prompt, catalogue dictionary, and function for
    a chosen business.

------------------------------------------------------------------------

**Workshop:** AI Agents -- Level 1, Day 2
