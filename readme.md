Messages
Definition: 
The messages parameter defines the conversation's context. It contains a list of messages with roles like system, user, and assistant, along with the respective content.
Example:
messages = [
    {"role": "system", "content": "You are a helpful assistant."},
    {"role": "user", "content": "What is the capital of France?"},
]
Purpose: Keeps track of the conversation, enabling contextual understanding.
Result: The assistant will reply, "The capital of France is Paris."
2. Model
Definition: 
Specifies the model to use for generating completions.
Options: Examples include gpt-4, gpt-3.5-turbo.
Example:
model = "gpt-4"
Purpose: Selects the level of capability for the assistant. gpt-4 is more powerful than gpt-3.5-turbo.
3. Max Completion Tokens
Definition: 
The maximum number of tokens (words, characters, punctuation, etc.) the model can generate in the output.
Example:
max_tokens = 100
Purpose: Controls the length of the assistant's response.
Result: Limits the output length to approximately 100 words or shorter.
4. n
Definition: 
Specifies how many completions the API should generate per request.
Example:
n = 3
Purpose: Returns multiple responses for the same input to provide variations.
Result: The assistant generates 3 possible responses for you to choose from.
5. Stream
Definition: 
If set to True, the API streams back results as they are generated (token by token), similar to a typing effect.
Example:
stream = True
Purpose: Makes interaction appear dynamic, useful for chat-like applications.
Result: The response arrives incrementally, creating a "typing" animation effect.
6. Temperature
Definition: 
Controls randomness in the model's responses. Higher values result in more random outputs.
Range: 0.0 (deterministic) to 1.0 (more creative).
Example:
temperature = 0.7
Purpose: Adjusts the "creativity" of the response.
Result: At temperature=0.0, the assistant gives the most probable and consistent answer. At temperature=1.0, it may generate more diverse or creative responses.
7. Top_p
Definition: 
A probability-based filter for response randomness. Combines with temperature to control diversity.
Range: 0.0 to 1.0 (higher means broader choice).
Example:
top_p = 0.9
Purpose: Limits the responses to a subset of likely options by focusing on the most probable outputs.
Result: With top_p=0.1, only the top 10% of probable responses are considered.
8. Tools
Definition: 
Additional plugins or tools that the assistant can access during the conversation.
Example:
tools = ["calculator", "code_execution"]
Purpose: Enhances the assistant's capabilities by enabling access to external functionalities, such as performing calculations or generating images.
Result: The assistant can solve math problems or execute Python code if equipped with appropriate tools.
