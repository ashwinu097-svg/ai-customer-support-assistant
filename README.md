# AI Customer Support Agent with Tool Calling

## 1. Project Overview
This project uses an AI agent to answer customer questions, check order statuses, and prepare escalation emails for human support.

## 2. Technologies Used
- Python
- LangChain
- LangGraph
- Cohere LLM
- Cohere Embeddings
- FAISS Vector Database
- Jupyter Notebook

## 3. Main Features
1. **FAQ Search:** Searches the FAQ knowledge base to answer customer questions.
2. **Order Status Lookup:** Checks mock order information using an order ID.
3. **Human Escalation:** Drafts an escalation email for complaints requiring human support.
4. **Conversation Memory:** Uses LangGraph InMemorySaver to retain conversation history within a thread.

## 4. Project Files
- `AI_Customer_Support_Agent.ipynb` — Main project notebook.
- `data/faq.txt` — Customer support FAQ knowledge base.
- `.env` — Stores the Cohere API key.

## 5. How It Works
1. The customer asks a question.
2. The AI agent determines which tool is appropriate.
3. The selected tool retrieves FAQ information, looks up an order, or drafts an escalation email.
4. The agent returns a response to the customer.

## 6. How to Run
1. Open the project folder in VS Code.
2. Activate the project's `.venv` kernel in Jupyter.
3. Ensure the required packages are installed.
4. Set `COHERE_API_KEY` in the `.env` file.
5. Run the notebook cells in order, from setup to testing.

## 7. Expected Outcome
A customer support assistant that answers FAQ questions, checks mock orders, drafts escalation emails, and supports conversation memory.

## 8. Limitations and Future Improvements

### Current Limitations
- Order information is stored in mock Python data, not a live order-management system.
- The FAQ knowledge base depends on the information available in `data/faq.txt`.
- Conversation memory uses `InMemorySaver` and is not permanent across kernel restarts.
- The escalation tool drafts an email but does not send it automatically.

### Future Improvements
- Connect to a real order-management API.
- Add a Streamlit user interface.
- Store conversation history persistently.
- Integrate an email service for approved escalations.
- Add logging, error handling, and automated tests.