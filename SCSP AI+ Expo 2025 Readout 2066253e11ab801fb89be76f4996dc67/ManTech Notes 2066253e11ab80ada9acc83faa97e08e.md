# ManTech Notes

- ManTech is Public→ Private with 3 branches: Civilian, Intelligence, and Defense
- All of the stack, data engineering, data science, AI, etc, all play a part.
- **Cyber:** Survivability and resilience. There is work on cyber operations, even looking into more frontier innovations on things like MCP.

**Secure Design and Implementation** 

A mostly architectural talk, a data centric view. 

- Three key questions: How is access to the data controlled? Where is the dat moved during processing? How long is data kept in each of the locations?
- Focus: Generative AI
    - NFS: Thank GOD that Dr. Summers knows what she’s talking about. Great explanations of different types of AI. Brief but clear (IMO)
- Types of data: how will AI use my data?
    - Distinction between prompt data, reference data, training and evaluation data. We’re going to be talking about mostly reference data today.
- **Generative AI by default**: “Conventional Wisdom”. The user acts as the interface with that conventional wisdom and specific use case.
    - **Cyber perspective**: really just one layer of control, a simple authentication.
    - Context caching for performance.
    - **Typical Consumer Use:** most providers DO really just take your data.
- **GENAI** **with fine tuning:** Providing specific, additional examples.
    - Once you fine tune the model, it is TREMENDOUSLY more difficult to hold back responses. It comes with all the problems of regular prompt hacking, jailbreaks.
    - The access to the fine tuned models should be treated at the same tier of the access controlled data that was used to create it.
- **RAG: “Not training from an AI perspective, just to be clear”**
    - A quick explanation of RAG.
    - It comes more down to access to the data store. When you add a RAG system, it ends up duplicating the system requirements, since this is just an operator.
- **Distributed RAG:** Multiple data sources.
    - Not just a single vector data store. Information doesn’t just have to come from a central location. It adds more work to the orchestrator, because the orchestrator will have to decide which is relevant + access controls there.
- **Additional Augmentation Methods**
    - Could include knowledge representations in addition to retrieval. Data models or hierarchy. GraphRAG, a knowledge graph.
        - Able to pull up more relevant material from indirect relationships.
        - You might not have a knowledge graph, but it might makes sense to derive one. Can use generative AI to derive a knowledge graph, which would later enhance the augmentation.
        - GraphRAG open-source from Microsoft
    - Example for ai+: Prompting it to look for the common themes of the ai+ expo? In singular documents and in single lookups, that would not be possible. But with a knowledge graph, this would be possible.
    - **Cyber:** The creation of the knowledge graph has information from the entirety of the dataset. Even post filtering messages could reveal knowledge about the knowledge graph.
        - Side note: the speakers mention how much we don’t speak on how much power the AI uses.
- **In general, for RAG, implement access control at retrieval time for end user on embeddings and text. Can use previous access controls.**
    - **Knowledge graphs can be treated the same way.**
- **Shared Resources**
    - Balance between shared and per-user basis, which switches based on the task. With code assist, its more user facing, but with RAG, it’s mostly shared.
    - **MCP:** passing tool descriptions (could be poisoned), prompt templates (executing malicious commands), tool name collisions. Insecure auth. Scope privileges. Cross connector attacks.
        - Extremely unsafe.
- **General Principles:**
    - More fine grained: keep access closer to the data source.
    - Derived data representations inherit controls.
    - Prefer augmentation over fine-tuning, adds another layer of interpretable control.

- Suggestions for distributed rag: with data repositories with multiple controls, consider creating a vector data base for each store.