# SmartLLMChain for Complex Queries :brain:

# ⚠️ Warning ⚠️

This feature has extreme potential to be relatively expensive. It uses a 3 step check and verify thought process that iterates through each step.

Here is the original creators example:

As example question, we will use "I have a 12 liter jug and a 6 liter jug. I want to measure 6 liters. How do I do it?". This is an example from the original SmartGPT video (https://youtu.be/wVzuvf9D9BU?t=384). While this seems like a very easy question, LLMs struggle do these kinds of questions that involve numbers and physical reasoning.

Example output:

```
> Entering new SmartLLMChain chain...
    Prompt after formatting:
    I have a 12 liter jug and a 6 liter jug. I want to measure 6 liters. How do I do it?
    Idea 1:
    1. Fill the 6-liter jug completely.
    2. Pour the water from the 6-liter jug into the 12-liter jug.
    3. Fill the 6-liter jug again.
    4. Carefully pour the water from the 6-liter jug into the 12-liter jug until the 12-liter jug is full.
    5. The amount of water left in the 6-liter jug will be exactly 6 liters.
    Idea 2:
    1. Fill the 6-liter jug completely.
    2. Pour the water from the 6-liter jug into the 12-liter jug.
    3. Fill the 6-liter jug again.
    4. Carefully pour the water from the 6-liter jug into the 12-liter jug until the 12-liter jug is full.
    5. Since the 12-liter jug is now full, there will be 2 liters of water left in the 6-liter jug.
    6. Empty the 12-liter jug.
    7. Pour the 2 liters of water from the 6-liter jug into the 12-liter jug.
    8. Fill the 6-liter jug completely again.
    9. Pour the water from the 6-liter jug into the 12-liter jug, which already has 2 liters in it.
    10. Now, the 12-liter jug will have exactly 6 liters of water (2 liters from before + 4 liters from the 6-liter jug).
    Idea 3:
    1. Fill the 6-liter jug completely.
    2. Pour the water from the 6-liter jug into the 12-liter jug.
    3. Fill the 6-liter jug again.
    4. Carefully pour the water from the 6-liter jug into the 12-liter jug until the 12-liter jug is full.
    5. The amount of water left in the 6-liter jug will be exactly 6 liters.
    Critique:
    Idea 1:
    1. Fill the 6-liter jug completely. (No flaw)
    2. Pour the water from the 6-liter jug into the 12-liter jug. (No flaw)
    3. Fill the 6-liter jug again. (No flaw)
    4. Carefully pour the water from the 6-liter jug into the 12-liter jug until the 12-liter jug is full. (Flaw: The 12-liter jug will never be full in this step, as it can hold 12 liters and we are only pouring 6 liters into it.)
    5. The amount of water left in the 6-liter jug will be exactly 6 liters. (Flaw: This statement is incorrect, as there will be no water left in the 6-liter jug after pouring it into the 12-liter jug.)
    
    Idea 2:
    1. Fill the 6-liter jug completely. (No flaw)
    2. Pour the water from the 6-liter jug into the 12-liter jug. (No flaw)
    3. Fill the 6-liter jug again. (No flaw)
    4. Carefully pour the water from the 6-liter jug into the 12-liter jug until the 12-liter jug is full. (Flaw: The 12-liter jug will never be full in this step, as it can hold 12 liters and we are only pouring 6 liters into it.)
    5. Since the 12-liter jug is now full, there will be 2 liters of water left in the 6-liter jug. (Flaw: This statement is incorrect, as the 12-liter jug will not be full and there will be no water left in the 6-liter jug.)
    6. Empty the 12-liter jug. (No flaw)
    7. Pour the 2 liters of water from the 6-liter jug into the 12-liter jug. (Flaw: This step is based on the incorrect assumption that there are 2 liters of water left in the 6-liter jug.)
    8. Fill the 6-liter jug completely again. (No flaw)
    9. Pour the water from the 6-liter jug into the 12-liter jug, which already has 2 liters in it. (Flaw: This step is based on the incorrect assumption that there are 2 liters of water in the 12-liter jug.)
    10. Now, the 12-liter jug will have exactly 6 liters of water (2 liters from before + 4 liters from the 6-liter jug). (Flaw: This conclusion is based on the incorrect assumptions made in the previous steps.)
    
    Idea 3:
    1. Fill the 6-liter jug completely. (No flaw)
    2. Pour the water from the 6-liter jug into the 12-liter jug. (No flaw)
    3. Fill the 6-liter jug again. (No flaw)
    4. Carefully pour the water from the 6-liter jug into the 12-liter jug until the 12-liter jug is full. (Flaw: The 12-liter jug will never be full in this step, as it can hold 12 liters and we are only pouring 6 liters into it.)
    5. The amount of water left in the 6-liter jug will be exactly 6 liters. (Flaw: This statement is incorrect, as there will be no water left in the 6-liter jug after pouring it into the 12-liter jug.)
    Resolution:
    1. Fill the 12-liter jug completely.
    2. Pour the water from the 12-liter jug into the 6-liter jug until the 6-liter jug is full.
    3. The amount of water left in the 12-liter jug will be exactly 6 liters.
    
    > Finished chain.





    '1. Fill the 12-liter jug completely.\n2. Pour the water from the 12-liter jug into the 6-liter jug until the 6-liter jug is full.\n3. The amount of water left in the 12-liter jug will be exactly 6 liters.'
```

For more information on this idea you can read the [langchain](https://python.langchain.com/docs/use_cases/more/self_check/smart_llm) documentation.

## Overview
This Streamlit application leverages the SmartLLMChain to handle complex and hard queries. Users can input difficult questions, and the application utilizes GPT-4 to generate insightful responses.

## Key Components

### Imports
- `streamlit`: Web application framework.
- `PromptTemplate`: To create prompt templates for the language model.
- `ChatOpenAI`: OpenAI's chat model.
- `SmartLLMChain`: Smart language model chain for handling complex queries.
- `StreamlitCallbackHandler`: To handle Streamlit callbacks.
- `ConversationalRetrievalChain`: For conversational retrieval in the assistant.
- `dotenv`: To load environment variables.
- `os`: Operating system functionalities.

### Functionality
- Utilizes SmartLLMChain to break down complex queries and generate responses.
- Users can input complex questions via a chat interface.
- Uses GPT-4 for generating responses to hard queries.

## Usage
1. Run miniAGI
2. Input a complex or hard question in the chat input.
3. View the assistant's generated response.

## Future Work
- Extend the SmartLLMChain for even more complex queries.
- Implement additional features such as follow-up questions and clarifications.


