# Conversational-RAG

Utilizing LangChain and Streamlit, I developed a Conversational RAG system that not only handles PDF documents but also maintains a dynamic chat history. When I asked the system to provide a detailed summary of our conversation, it flawlessly returned the chat we had 

Here's how I made it happen
𝗘𝗺𝗯𝗲𝗱𝗱𝗶𝗻𝗴 𝗚𝗲𝗻𝗲𝗿𝗮𝘁𝗶𝗼𝗻: Employed Hugging Face's all-MiniLM-L6-v2 model to generate embeddings, providing a robust foundation for document retrieval.

𝗣𝗗𝗙 𝗗𝗼𝗰𝘂𝗺𝗲𝗻𝘁 𝗣𝗿𝗼𝗰𝗲𝘀𝘀𝗶𝗻𝗴: Implemented a file uploader for PDFs, allowing users to upload multiple files.
Leveraged PyPDFLoader for loading and parsing PDF documents into a manageable format.

𝗗𝗼𝗰𝘂𝗺𝗲𝗻𝘁 𝗦𝗽𝗹𝗶𝘁𝘁𝗶𝗻𝗴: Used RecursiveCharacterTextSplitter to split documents into smaller, overlapping chunks

𝗥𝗲𝘁𝗿𝗶𝗲𝘃𝗲𝗿 𝗦𝗲𝘁𝘂𝗽: Integrated Chroma as a vector store for document embeddings, enabling efficient retrieval based on user queries.

𝗖𝗼𝗻𝘁𝗲𝘅𝘁𝘂𝗮𝗹𝗶𝘇𝗲𝗱 𝗤𝘂𝗲𝘀𝘁𝗶𝗼𝗻 𝗙𝗼𝗿𝗺𝘂𝗹𝗮𝘁𝗶𝗼𝗻: Developed a system prompt using ChatPromptTemplate to reformulate user questions into standalone queries, ensuring clarity without chat history dependency.

𝗛𝗶𝘀𝘁𝗼𝗿𝘆-𝗔𝘄𝗮𝗿𝗲 𝗥𝗲𝘁𝗿𝗶𝗲𝘃𝗮𝗹: Created a history-aware retriever to maintain context across interactions, crucial for providing accurate and contextual answers.

𝗤𝘂𝗲𝘀𝘁𝗶𝗼𝗻-𝗔𝗻𝘀𝘄𝗲𝗿𝗶𝗻𝗴 𝗖𝗵𝗮𝗶𝗻: Built a QA chain using LangChain's document combination tools, ensuring concise and relevant responses.

𝗦𝗲𝘀𝘀𝗶𝗼𝗻 𝗠𝗮𝗻𝗮𝗴𝗲𝗺𝗲𝗻𝘁: Implemented session-based chat history management to track conversation context, enhancing user experience.

𝗖𝗼𝗻𝘃𝗲𝗿𝘀𝗮𝘁𝗶𝗼𝗻𝗮𝗹 𝗥𝗔𝗚 𝗖𝗵𝗮𝗶𝗻 𝗘𝘅𝗲𝗰𝘂𝘁𝗶𝗼𝗻: Combined all components into a RunnableWithMessageHistory, allowing dynamic interaction with the model while maintaining chat history.
